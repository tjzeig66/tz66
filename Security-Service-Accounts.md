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

Password Policy Test 
[Password Policy Test](screenshots/password-policy-test.png)
