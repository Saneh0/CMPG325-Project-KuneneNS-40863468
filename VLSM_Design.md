# VLSM Addressing Plan

**Assigned Address Block:** 172.30.6.0/23 (Total 512 IPs)

To efficiently allocate IP addresses for the Reaboka Early Childhood Development Centre, Variable Length Subnet Masking (VLSM) was used. The subnets were allocated from largest to smallest based on the device requirements of each department.

| Department | Devices Needed | Subnet Size | Subnet Mask | Network Address | Usable IP Range | Broadcast Address |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **Classrooms (VLAN 10)** | 50 | /26 (64 IPs) | 255.255.255.192 | 172.30.6.0 | 172.30.6.1 - .62 | 172.30.6.63 |
| **Admin (VLAN 20)** | 20 | /27 (32 IPs) | 255.255.255.224 | 172.30.6.64 | 172.30.6.65 - .94 | 172.30.6.95 |
| **Staff Wi-Fi (VLAN 30)** | 20 | /27 (32 IPs) | 255.255.255.224 | 172.30.6.96 | 172.30.6.97 - .126 | 172.30.6.127 |
| **Server Room (VLAN 40)** | 5 | /29 (8 IPs) | 255.255.255.248 | 172.30.6.128 | 172.30.6.129 - .134 | 172.30.6.135 |

### Router Gateway IPs:
- **Classroom Gateway:** 172.30.6.1
- **Admin Gateway:** 172.30.6.65
- **Staff Wi-Fi Gateway:** 172.30.6.97
- **Server Gateway:** 172.30.6.129
