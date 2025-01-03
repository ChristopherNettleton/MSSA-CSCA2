# Components Overview

## Servers
1. **MServerV1:**
   - Roles: DNS, DHCP, Microsoft SQL Database
   - IP Address: 192.168.1.1
   - Part of the failover cluster (MSV1MSV2Cluster).

2. **MServerV2:**
   - Role: Failover Cluster Node
   - IP Address: 192.168.1.2
   - Provides high availability for DNS, DHCP, and SQL services.

3. **MServerV3:**
   - Roles: Nested Hyper-V, Windows Admin Center, Minecraft Server
   - IP Address: 192.168.1.3

4. **CentOS Client:**
   - Role: Test client
   - IP Address: 192.168.1.101

## Key Features
- **Failover Cluster (192.168.1.4):**
  - Provides high availability for services hosted on MServerV1 and MServerV2.
- **DNS and DHCP:**
  - Configured on MServerV1 for domain and IP address management.
- **SQL Database:**
  - Hosted on MServerV1 for centralized data management.
- **Remote Access:**
  - Enabled for all servers to allow management from external devices.
- **File Sharing:**
  - Configured across all three MServers.
