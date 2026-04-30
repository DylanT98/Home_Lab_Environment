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


## Incident: Manual Account Lockout - User: Mscott
* **Issue:** User `Mscott` was unable to log in to the workstation (**Winserv**). System returned the error: "The referenced account is currently locked out."
* **Diagnosis:** * Checked the Security Logs in **Event Viewer** on the Domain Controller.
    * Filtered for **Event ID 4740**.
    * Confirmed the lockout was triggered locally on the workstation **Winserv** due to multiple failed logon attempts.
* **Root Cause:** Manual entry of incorrect credentials exceeded the 'Account Lockout Threshold' (3 attempts) defined in the Default Domain Policy.
* **Resolution:** * Navigated to **Active Directory Users and Computers**.
    * Located the `Mscott` user object and accessed **Account Properties**.
    * Checked the **"Unlock account"** box and applied changes.
    * Verified successful login on the **Winserv** workstation.
* **Status:** Resolved
* <img width="2558" height="1439" alt="AccountLockout1" src="https://github.com/user-attachments/assets/e04e3d5d-fb4a-4db0-9f5e-32bdf4a9f828" />
* <img width="2559" height="1439" alt="accountlockout2" src="https://github.com/user-attachments/assets/185b8153-e580-4c11-848b-9882aa8d609a" />


