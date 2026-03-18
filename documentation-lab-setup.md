# Active Directory Lab Documentation 

## 1. Organizational Unit (OU) Structure
Domain

-US
  - Users
  - Computers
  - Servers

-Europe
  - Users
  - Computers
  - Servers

-Asia
  - Users
  - Computers
  - Servers

[OU Structure](screenshots/ad-ou-structure.png)
## 2. Security & Distribution Groups
### Europe
-EU-DL-AllEmployees

-EU-DL-ITAdmins

-EU-IT

-EU-EastCharmer 
... (US and Asia same input)

[Security & Distribution Groups](screenshots/security-distribution-groups.png)
## 3. Group Policy Objects (GPOs)
**Applied and tested on client machines**

- Default Domain Controllers Policy
- Default Domain Policy
- Desktop Wallpaper
- Disable USB devices
- Drive Mapping
- Password policy
- Restrict Control Panel
  
[GPOs](screenshots/gpo-example.png)
