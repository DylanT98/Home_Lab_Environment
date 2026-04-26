## Lab Infrastructure Expansion
* **Objective:** Establish a multi-machine domain environment.
* **Network Strategy:** Utilizing Bridged Adapter on all VMs to ensure local network parity.
* **Planned Services:** * Domain Controller (Active Directory DS)
    * DHCP Server (Dynamic IP management for client pool)
* **Status:** Network infrastructure verified and ready for client deployment.

### Network Configuration
* **Status:** Static IPv4 assigned (192.168.0.200).
* **Troubleshooting Note:** Initially lost connectivity due to a gateway mismatch between the VM (10.x.x.x) and the physical network (192.168.0.x). Resolved by updating the VirtualBox adapter to 'Bridged' mode and manually configuring the Gateway to match the home router (192.168.0.1).

<img width="2559" height="1439" alt="Ip configuring" src="https://github.com/user-attachments/assets/6c7e06e6-8451-483d-b91f-932696093ca9" />


