## 3. Group Policy Objects (GPOs)

###Process Demonstration

### Control Panel Restriction GPO

Configured a Group Policy Object to restrict access to the Control Panel for standard VM client created later

Path:
User Configuration -> Policies -> Administrative Templates -> Control Panel

Setting:
- Prohibit access to Control Panel and PC settings: Enabled

[Control Panel Policy Configuration](screenshots/control-panel-policy-config.png)

### Desktop Wallpaper Restrictions GPO

Configured a Group Policy Object to prevent users from changing the desktop wallpaper, enforcing a standardized desktop environment across domain-joined machines

Path:
User configuration -> Policies -> Administrative Templates -> Desktop -> Desktop Wallpaper

Setting:
- Prevent changing desktop background: Enabled

  [Wallpaper Policy Configuration](screenshots/wallpaper-policy-config.png)

### Password Policy Configuration GPO

Configured password policy settings to enforce domain-wide password complexity and security requirements via the Default Domain Policy

Path:
Computer Configuration -> Policies -> Windows Settings -> Security Settings -> Account Policies -> Password Policy

Settings:
-Minimum password length: Configured (12 characters)
-Password must meet complexity requirements: Enabled
-Maximum password age (90 days)
-Minimum password age (30 days) set automatically when maximum password age was set

[Password Policy Configuration](screenshots/password-policy-config.png)



The following steps were 
**Configured Group Policy Objects GPOs**

- Default Domain Controllers Policy
- Default Domain Policy
- Desktop Wallpaper
- Disable USB devices
- Drive Mapping
- Password policy
- Restrict Control Panel
  
[GPOs](screenshots/gpo-examples.png)

## 4. Applied & Tested GPOs on Client Machines

### Group Policy Objects Applied to Client VM

[GPOs Applied](screenshots/GPOs-applied-client.png)

### Disable Wallpaper via GPO

[Disable Wallpaper](screenshots/GPO-disable-wallpaper.png)

### Disable Client Access to Control Panel

[Disable Access to Control Panel](screenshots/GPO-control-panel-restrictions.png)
