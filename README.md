# -LAB-Security-policies Implement a password policy
Security policies outline measures to protect sensitive data from unauthorized access, disclosure, modification, and destruction. 


**Learning objectives**
* Define the significance of security policies in protecting organizational assets
* Identify key components of security policies
* Investigate how security policies contribute to access control mechanisms and authentication processes
* Implement security policy enforcement mechanisms


**Devices**
  
The lab contains one virtual machine:
ZYWIN01 (Windows Server 2022)

**Tasks**

Task 1: Implement a password policy

Task 2: Implement an audit policy

Task 3: Implement an antivirus policy


## Task 1: Implement a password policy

In Task 1, a password policy is implemented in Windows Server to meet the following requirements:

* Password must be a minimum of 8 characters

* Users must be locked out for 30 minutes after failing to logon 5 times in a row

* Users may not reuse any of the users' last 3 passwords

* Users must change passwords every 60 days

**Select ZYWIN01 from the drop-down menu in the right pane and click Connect to VM.**

<img width="1096" height="790" alt="image" src="https://github.com/user-attachments/assets/88a0eb1a-2b0c-4173-9c66-75254cf46872" />

**Click Windows Start and select Server Manager.**

<img width="415" height="697" alt="image" src="https://github.com/user-attachments/assets/8019ce7c-3072-4151-8c35-9c4a4a3d8751" />

**In Server Manager, select Tools → Group Policy Management.**

<img width="689" height="288" alt="image" src="https://github.com/user-attachments/assets/67106f88-0a45-4618-9eb4-ac9bd1ba7b8f" />

**In Group Policy Management console, click Default Domain Policy under mycompany.com.**

<img width="685" height="494" alt="image" src="https://github.com/user-attachments/assets/dee05a69-374c-4e39-817b-110e172c6274" />

**Click OK to acknowledge changes made to the default domain policy are global to the GPO.**

<img width="475" height="189" alt="image" src="https://github.com/user-attachments/assets/af0fe125-697e-4a05-a754-8ea4c555a1de" />

**Right-click Default Domain Policy under mycompany.com and select Edit.**

<img width="681" height="488" alt="image" src="https://github.com/user-attachments/assets/192e0d51-e17a-46e2-ad0e-64975cc47d8b" />

**In Group Policy Management Editor, navigate to Computer Configuration → Policies → Windows Settings → Security Settings → Account Policies → Password Policy.**

<img width="683" height="552" alt="image" src="https://github.com/user-attachments/assets/c12af2c7-3162-4694-9b5e-4c1b1267ef6a" />

**Double-click Minimum password length, enter 8 in the Password must be at least: list box, and click OK.**

<img width="462" height="551" alt="image" src="https://github.com/user-attachments/assets/db65b76c-f63f-4760-8007-76e5fb7a4be2" />

**By default, changes made to group policies are applied every 90 mins. gpupdate is a command-line utility for updating group policies on-demand.**

**In a PowerShell window, run gpupdate.**

<img width="688" height="284" alt="image" src="https://github.com/user-attachments/assets/d4ac1e41-b547-4634-a0a1-7817e9a824d9" />

**In Group Policy Management Editor, double-click Maximum password age.**

<img width="677" height="553" alt="image" src="https://github.com/user-attachments/assets/8c9c6f4b-9c6b-433f-81ba-31b81530aa50" />

**Enter 60 in the Password will expire in: list box, and click OK.**

<img width="543" height="646" alt="image" src="https://github.com/user-attachments/assets/e943fecf-2b87-46d8-ac6a-cd0134d03cb8" />

**Update group policies by running gpupdate in a PowerShell window.**

**Maximum password age set to 60.**

<img width="957" height="195" alt="image" src="https://github.com/user-attachments/assets/fa2f2a6c-c194-4401-982e-e1c03c9e76c0" />

**In Group Policy Management Editor, double-click Enforce password history.**

<img width="683" height="545" alt="image" src="https://github.com/user-attachments/assets/571b9773-d068-44e4-a174-70592f4a6f9d" />

**Enter 3 in the Keep password history for: list box, and click OK.**

<img width="612" height="678" alt="image" src="https://github.com/user-attachments/assets/7d115985-3659-4332-9415-5dc2619330bb" />

**Update group policies by running gpupdate in a PowerShell window.**

**Password history count set to 3.**

<img width="950" height="166" alt="image" src="https://github.com/user-attachments/assets/2f50edbd-18df-4931-8c01-848dd0e01403" />

**In Group Policy Management Editor, select Account Lockout Policy in the left pane and double-click Account lockout threshold in the right pane.**

<img width="684" height="549" alt="image" src="https://github.com/user-attachments/assets/8a3f2150-9573-4e0f-b33a-aed1b2804b47" />

**Enter 5 invalid logon attempts in the Account will lock out after: list box and click OK.**

<img width="542" height="666" alt="image" src="https://github.com/user-attachments/assets/a76fa754-eba1-43ac-9e30-fd3b01318008" />

**Click OK in the Suggested Value Changes window.**

<img width="574" height="305" alt="image" src="https://github.com/user-attachments/assets/a14a6cf9-f9e9-4792-a69d-dfeaf15a6a66" />

**Update group policies by running gpupdate in a PowerShell window.**

**Account lockout threshold set to 5.**

<img width="613" height="122" alt="image" src="https://github.com/user-attachments/assets/57eb932e-bfb2-42c2-b425-344504cdc2d4" />

**In Group Policy Management Editor, double-click Account lockout duration.**

<img width="684" height="559" alt="image" src="https://github.com/user-attachments/assets/5d99d420-3f17-4a8d-ab93-7e04254132cc" />

**Click the Define this policy setting checkbox, enter 30 minutes in the Account is locked out for: list box, and click OK.**

<img width="456" height="555" alt="image" src="https://github.com/user-attachments/assets/c7ee66b7-f5b0-48a3-be48-68a5e26f289c" />

**Update group policies by running gpupdate in a PowerShell window.**

**Account lockout duration set to 30 minutes.**

<img width="509" height="79" alt="image" src="https://github.com/user-attachments/assets/44340fcb-e1d5-4168-85c8-53c5752f370a" />
















  

