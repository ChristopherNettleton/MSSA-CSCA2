# Virtual Switch Setup

## Creating an Internal Switch
1. Open Hyper-V Manager.
2. Click on **Virtual Switch Manager** in the right-hand pane.
3. Select **New virtual network switch** > **Internal** > **Create Virtual Switch**.
4. Name the switch `Server Internal Switch` and save the configuration.

## Creating an External Switch
1. Open Hyper-V Manager.
2. Click on **Virtual Switch Manager** in the right-hand pane.
3. Select **New virtual network switch** > **External** > **Create Virtual Switch**.
4. Name the switch `VM Connection`.
5. Assign the switch to the physical network adapter and save the configuration.

## Assigning Switches to VMs
1. Open the **Settings** for each virtual machine in Hyper-V Manager.
2. Under **Network Adapter**, select the appropriate virtual switch:
   - Server Internal Switch for internal communication.
   - VM Connection for external access.
