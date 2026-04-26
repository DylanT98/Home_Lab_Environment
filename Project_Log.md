## AD DS Domain Controller Deployment
* **Objective:** Establish the foundation for a centralized identity management environment using a root domain of `lab.test`.
* **Infrastructure Role:** Active Directory Domain Services (AD DS) & DNS.
* **Key Steps:**
    * Promoted the member server to a Domain Controller.
    * Configured a new forest (`lab.test`) to centralize authentication and security.
    * Integrated DNS services to ensure internal name resolution for domain-joined clients.
* **Status:** Completed.
* **Outcome:** Successfully established a root domain controller, enabling centralized user authentication, group policy management, and organizational structure via Organizational Units (OUs).

Domain Controller Setup <img width="2559" height="1439" alt="DomainControllerSetup" src="https://github.com/user-attachments/assets/c67879ba-d5a2-4980-aa9c-f68089b3cc03" />



## [2026-04-26] Security Policy: Password Compliance Baseline
* **Objective:** Implement an enterprise-standard password security baseline to mitigate credential-based attacks.
* **Configuration:**
    * **Maximum password age:** 30 days.
    * **Minimum password length:** 10 characters.
    * **Enforce password history:** 5 passwords.
* **Key Steps:** * Modified the Default Domain Policy GPO within Group Policy Management.
    * Validated policy application on client machine using `gpupdate /force` and `net accounts`.
* **Status:** Completed.
* **Outcome:** Successfully enforced organizational security compliance, preventing password reuse and reducing risk associated with weak or stagnant credentials.

<img width="2559" height="1439" alt="PasswordManagement" src="https://github.com/user-attachments/assets/48e113c3-590d-4105-a699-7912d9c0e4b6" />

