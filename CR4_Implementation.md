# Change Request 4 (CR4) Implementation

**Change Request:** A new application/file server is installed and must be reachable by authorised departments only.

### Implementation Strategy
To enforce this security requirement, an **Extended Access Control List (ACL)** was configured on the router (Router-on-a-Stick). 

- **Authorized:** Admin Department (VLAN 20)
- **Unauthorized:** Classrooms (VLAN 10) and Staff Wi-Fi (VLAN 30)

### Router Configuration Commands
The following ACL was created and applied to the Server VLAN sub-interface:

```text
ip access-list extended BLOCK_SERVER
! Deny Classrooms from reaching the Server
deny ip 172.30.6.0 0.0.0.63 172.30.6.128 0.0.0.7
! Deny Staff Wi-Fi from reaching the Server
deny ip 172.30.6.96 0.0.0.31 172.30.6.128 0.0.0.7
! Permit Admin to reach the Server
permit ip 172.30.6.64 0.0.0.31 172.30.6.128 0.0.0.7
exit

interface gigabitEthernet 0/0.40
ip access-group BLOCK_SERVER out
exit
