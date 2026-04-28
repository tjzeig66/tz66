### Set up File Sharing with appropriate permissions

This section demonstrates how to configure a shared folder on the domain controller and apply both Share and NTFS permissions to allow acccess from domain-joined client machines

---

###  Create Shared Folder

1. Log into Domain Controller
2. Navigate to a local disk (C:)
3. create new folder inside called SHARED

### Configure Share Permissions (Network Level)

1. Right click the 'SHARED' folder and head to **Properties**
2. Go to the Sharing tab and click **Advanced Sharing**
3. Check the **Share this Folder** checkmark and click on **Permissions**
4. Click Permissions and click Remove 'Everyone' and Add 'Domain Users'

### Configure NTFS Permissions (File System Level)

1. Switch to the **Security** tab
2. Click **Edit** and then **Add**
3. Type 'Domain Users' and click **OK**

### Verification (Client Side)

1. Log into the client VM as a Domain User
2. Open file explorer
3. Right-click **This PC** and click on **Map Network Drive**
4. Set Drive letter to S:  and type in type in path for the folder created (\\servername\SHARED)

 ## Troubleshooting: VM Reboot Shared File Missing
 
## **Problem** 
Once the client VM is rebooted access to the shared file created and mapped is gone so if users were wanting to access the shared file they would have to redo those steps each time.
### **The Fix**
To resolve this, you have to configure a GPO to automatically map network drives for users:

1. Go to Group Policy Management on Domain Controller and make a new GPO called **Mapped Drives** and click **Edit**
2. Path: User Configuration --> Preferences -->Window Settings --> Drive Maps -->>new mapped drive
3. type in \\servername\SHARED
4. and make drive letter S:
5. Drag and drop the newly made GPO in the Users section of one of the regions (US)
