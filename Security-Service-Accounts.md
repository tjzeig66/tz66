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

   [Account Lockout Policy](screenshots/account-lockout.png)

   ---

  ### Assign & Restrict User Rights

1. Open Group Policy Management Console
2. Right click Default Domain Policy and click edit
3. Navigate this path:
Computer Configuration -> Policies -> Windows Settings -> Security Settings -> Local Policies -> User Rights Assignment

4. Configure restrictions for:

- Allow log on locally

[User Deny Login](screenshots/user-rights-deny-login.png)

- Allow log on through Remote Desktop Services

[User Rights RDP](screenshots/user-rights-allow-RDP.png)

---

### Implementation of Fine-Grained Password Policies

1. Open Active Directory Administrative Center on the Domain Controller
2. Once in click on domain name to the left and follow path: system -> Password Settings Container
3. Once in Password Settings click on **New** create password policy for admins or regular users
4. select name and policy with clear name and change the precedence of the password (which determines the order in which policy objects are applied)
5. You can also change minimum password length, password history, and password complexity

[Fine-Grained Password Policy](screenshots/fine-grained-password-policy.png)
      
