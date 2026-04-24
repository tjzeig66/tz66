# Active Directory Structure & Domain Setup Page

A sample OU structure was created to demonstrated the implementation workflow within Active Directory.

The domain was organized into regional OUs to seperate users, computers, and servers by location.
### Process Demonstration

- Navigated to the domain container in ADUC called EastCharmer.local
- Created a new Organizational Units (OUs) for each region: US, Europe, and Asia
- Created child OUs (Users, Computers, Servers) within each regional OU

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

## Troubleshooting: Accidental Deletion Protection

## **Problem** 
When attempting to delete an incorrectly placed Organizational Unit (OU), the system blocked the action along with the following error message:
> *"You do not have sufficient privilges to delete Users, or this object is protected from accidental deletion."*
### **The Fix**
To resolve this, I had to bypass the default Active Directory safety constraints:

1. **Enable Advanced Features:** In the Active Directory Users and Computers (ADUC) console, I toggled on 'View > Advanced Features'.

   [Enabling Advanced Features](screenshots/advanced-features-view.png)
   *Enabling Advanced Features to expose hidden object attributes.*
   
2. **Direct Navigation:** I identified that the **Object** tab is hidden if the OU is found via "Search/Find" tool. I closed the search and manually navigated to the OU through the **Domain Tree"" sidebar.
  
3.  **Disable Protection**
   - Right-clicked the OU > Properties**.
   - Navigated to the now visible **Object** tab.
   - Unchecked **Protect object from accidental deletion."**

     [Disabling Protection](screenshots/OU-protection-fix.png)
     *Disabling the accidental deletion flag in the Object tab.*
     
   **Execution:** Successfully deleted the OU from the directory.
## 2. Security & Distribution Groups
  ### Process Demonstration
  
  - Navigated to Users child OU inside each region
  - then I right clicked and went to the New column and clicked Users
  -I then created users inside Users child OU called US-DL-AllEmployees, US-DL-ITAdmins, US-IT, and US-tjzeig.
  -Created exact same users inside the Users child OU for each  other region: Europe and Asia

### US
-US-DL-AllEmployees

-US-DL-ITAdmins

-US-IT

-US-tjzeig
... (US and Asia same input)

[Security & Distribution Groups](screenshots/security-distribution-groups.png)

