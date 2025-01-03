# Private Cloud Setup Documentation

This repository contains detailed documentation, configurations, and scripts for setting up a private cloud environment using Windows Server 2019 and CentOS.

## Features
- **Failover Cluster:** MServerV1 and MServerV2 configured for high availability.
- **Domain Integration:** All servers are part of the `MSSADomain.local`.
- **Services Hosted:**
  - MServerV1: DNS, DHCP, Microsoft SQL Database.
  - MServerV3: Nested Hyper-V, Windows Admin Center, and Minecraft Server.
- **CentOS Client Server:** A client server connected to the domain for testing and remote access.
- **Remote Access:** Enabled for all servers, with file sharing configured across the environment.

## Infrastructure Overview

| Server        | Role                                 | IP Address       |
|---------------|--------------------------------------|------------------|
| MServerV1     | DNS, DHCP, SQL Database, Failover   | 192.168.1.1      |
| MServerV2     | Failover Cluster Node               | 192.168.1.2      |
| MServerV3     | Nested Hyper-V, Admin Center, Minecraft Server | 192.168.1.3      |
| Cluster       | Failover Cluster Virtual IP         | 192.168.1.4      |
| CentOS Client | Client Server                       | 192.168.1.101    |

## Configuration Highlights
- **Failover Cluster**: `MSV1MSV2Cluster` ensures high availability for critical services.
- **Domain Name**: `MSSADomain.local` for centralized authentication and management.
- **User Accounts**: One user with full administrative privileges is configured.
- **Remote Access**: Enabled for all servers with file sharing.

## Repository Structure
