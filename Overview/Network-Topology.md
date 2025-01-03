# Network Topology

The private cloud network uses a combination of internal and external virtual switches for connectivity. Below are the details:

## Virtual Switches
1. **Internal Switch (InternalNet):**
   - Purpose: Allows communication between virtual machines within the private cloud and the host system.
   - Connected Systems:
     - MServerV1 (192.168.1.1)
     - MServerV2 (192.168.1.2)
     - MServerV3 (192.168.1.3)
     - CentOS Client (192.168.1.101)

2. **External Switch (ExternalNet):**
   - Purpose: Provides access to the physical network for internet connectivity and external device communication.
   - Connected Systems:
     - MServerV1 (192.168.1.1)
     - MServerV3 (192.168.1.3)

## IP Addressing
- **Subnet:** 192.168.1.0/24
- **Domain Name:** MSSADomain.local
- **Cluster Virtual IP:** 192.168.1.4
- **CentOS Client IP:** 192.168.1.101

## Server Connections
- **MServerV1:** Connected to both InternalNet and ExternalNet.
- **MServerV2:** Connected only to InternalNet for failover clustering.
- **MServerV3:** Connected to both InternalNet and ExternalNet for hosting Hyper-V VMs and the Minecraft server.
- **CentOS Client:** Connected to InternalNet for testing and domain services.

## Additional Notes
- The **VM Connection** External switch is bridged to the physical network adapter on the host machine, providing external connectivity.
- The **Server Internal Switch** Internal switch is isolated, ensuring secure communication between VMs without exposing internal traffic to the external network.
