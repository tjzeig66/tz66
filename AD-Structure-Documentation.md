# Active Directory Structure & Management Lab Documentation 

### Process Demonstration
A sample OU structure was created to demonstratre the implementation workflow within Active Directory.

The domain was organized into regional OUs to seperate users, computers, and servers by location.

-Navigated to the domain container in ADUC called EastCharmer.local
-Created a new Organizational Units (OUs) for each region: **US**, **Europe**, and **Asia**
-Created child OUs (**Users**, Computers, Servers**) within each regional OU

Below are screenshots of the outcome of the top-level OUs and child OUs

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

