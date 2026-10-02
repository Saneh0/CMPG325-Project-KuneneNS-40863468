# Testing Evidence

### 1. VLSM & DHCP Verification
The Admin PC successfully received an IP address from the DHCP pool within the assigned VLSM range.

![Admin DHCP Configuration](Admin_DHCP.png)
*(Figure 1: Admin PC receiving IP 172.30.6.66 via DHCP)*

### 2. Inter-VLAN Routing
The Admin PC can successfully communicate with other VLANs through the Router-on-a-Stick.

![Admin Ping Classroom](Admin_Ping_Classroom.png)
*(Figure 2: Successful ping from Admin to Classroom gateway)*

### 3. CR4 - Authorized Access (Success)
The Admin PC is authorized to access the new File Server.

![CR4 Authorized Success](CR4_Authorized_Success.png)
*(Figure 3: Successful ping from Admin PC to File Server)*

### 4. CR4 - Unauthorized Access (Blocked)
The Classroom PC is blocked from accessing the File Server due to the ACL.

![CR4 Unauthorized Fail](CR4_Unauthorized_Fail.png)
*(Figure 4: Ping from Classroom PC to File Server timing out as expected)*
