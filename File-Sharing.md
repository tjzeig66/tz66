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
