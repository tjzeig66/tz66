### Implemented Security Policies using Group Policy Management Console & Active Directory Administrative Center (ADAC)

--- 

### Configured password policy settings to enforce domain-wide password complexity and security requirements via the Default Domain Policy

1. Log into Domain Controller
2. Open Group Policy Management Console
3. Navigated to :
Computer Configuration -> Policies -> Windows Settings -> Security Settings -> Account Policies -> Password Policy

4. Configure
-Minimum password length: Configured (12 characters)

-Password must meet complexity requirements: Enabled

-Maximum password age (90 days)

-Minimum password age (30 days) set automatically when maximum password age was set

[Password Policy Configuration](screenshots/password-policy-config.png)


Password Policy Test:

[Password Policy Test](screenshots/password-policy-test.png)

---

### Configure Account Lockout Policy

1. Open Group Policy Management Console again
2. right click default domain policy and press edit
3. Navigate this path: Computer Configuration -> Policies -> Windows Settings -> Security Settings -> Account Policies -> Account Lockout Policy

4. Configure
  -Account Lockout Duration: 30 minutes
   -Account Lockout Threshold: 3 invalid attempts
   -Reset account lockout counter after: 30 minutes

   [Account Lockout Policy}(screenshots/account-lockout.png)
