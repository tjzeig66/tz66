# Active Directory Structure & Management Lab Documentation 

### Implementation Process

### OU Structure Implementation

#### Process Example
To demonstrate the creation of the Organizational Unit (OU) structure, a sample OU hierarchy was created within the domain.

- Created a top-level OU named **Test-Region**
- Created child OUs within Test-Region for:
  - Users
  - Computers
  - Servers
- Verified proper hierarchy and structure within Active Directory Users and Computers (ADUC)

**Screenshot 1 – OU Creation**  
Displays the creation of the **Test-Region** OU within the domain.

**Screenshot 2 – Child OU Structure**  
Displays the completed Test-Region OU with nested child OUs (Users, Computers, Servers).

---

#### Final Implementation
The production environment OU structure consists of three regional OUs:

- US  
- Asia  
- Europe  

Each region contains the following sub-OUs:
- Users  
- Computers  
- Servers  

This structure enables efficient administration and targeted Group Policy application across different regions.

**Screenshot 3 – Full OU Hierarchy**  
Displays the completed multi-region OU structure within the domain.

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

