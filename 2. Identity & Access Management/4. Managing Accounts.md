Account management is concerned with creating, managing, disabling and terminating accounts. When the account is active, access control methods are used to control what the user can do. Additionally, administrators use access controls to control when, where, and how users can log on.

## Credential Policies and Account Types
*Credential Policies* define login policies for different personnel, devices and accounts. The following list shows different account types and credential policies associated with each of them.

* **Personnel or end-user accounts**: Most accounts will be of this type. Admins will create these accounts and then assign appropriate privileges based on the user's job. Basic credentials policies like the min password length, password history and account lockouts.
* **Administrator and root accounts**: These privileged accounts have additional rights and privilege compared to regular user accounts. Credential policies require stronger authentication methods, such as MFA.
* **Service accounts**: Service accounts like an SQL user in Linux or MSSQL in Windows require long and secure passwords, they are similar to regular user accounts but these passwords should not expire, if they do the service will stop.
* **Device accounts**: Computers and other devices can also have account, think of computer accounts in AD. 
* **Third-party accounts**: These accounts come from external entities that have access to the network. These should have strong credential policies in place with strong password policies.
* **Guest accounts**: Similar to the guest account in windows, useful if you want to grant someone basic control over a system. Commonly disabled unless its required.
* **Shared and generic account/credentials**: Similar to guest accounts, imagine a temporary company needs an account, in that case a shared account can be used, this way we do not need an account for each temporary employee, can be more tailored compared to a guest account. Basic credential policies apply.

## Privileged Access Management 
*Privilege access management (PAM)* allows an organization to apply more strict security controls over accounts with elevated privileges, such as administrator accounts. PAM implements the concept of *just-in-time permissions*. This means that an admin account will have user level privileges until they require admin privileges. Think of UAC in Windows. The account will send a request, PAM will then add this user to the admin role for a time period after which the user will be removed from the group.

PAM also stores admin account passwords in a secure vault, which are set up in a ways that no human ever sees or accesses the password for an admin account. 

PAM is also able to create *temporary accounts* which have admin privileges and are automatically destroyed after a couple hours or the user finishes his task.

* Allow users to access the admin account without knowing the password
* Automatically change privileged account passwords periodically.
* Limit the time users can use the admin account
* Allow users to checkout credentials
* Log all access of credentials in a logfile

## Requiring Administrators to Use Two Accounts
It is common practice for admins to have two accounts, one which acts as normal user account for day-to-day work the other account has higher privileges and is used to perform administrative tasks. 

Imagine malware gets inside your computers, the malware will try to use privilege escalation to get to an admin account, if the administrator only uses his user account the malware will have a much harder time trying to priv esc.

## Prohibiting Shared and Generic Accounts
If multiple people are using the same account the basic concept of authentication is broken, this is because we can never know how performed which tasks since multiple people can login into the same account. Guest accounts are still fine to use if only one person is using them at a time. 

## Deprovisioning 
*Deprovisioning* is the process used to disable a user's account when they leave the organization. This process is either done by an administrator or automatically as soon as the user leaves the HR system. 

Disabling is often preferred over deleting the account. This is because encryption keys are inside the account, if we delete the account and a file is encrypted the organization will have lost the file. 

* **Terminated employee**: Accounts should be disabled ASAP to avoid ex-employees from wrecking havoc on the network.
* **Leave of absence**: If an employee will be absent for an extended period of time it is also common to disable his account
* **Account deletion**: When the organization determines that the account is not longer needed, administrators delete it.

## Time-Based Logins
*Time-based logins* ensure that users can only log on to computers during specific times. If a user decides to log on to a system outside the restricted time, the system will deny access to the user. 

An example could be a company that operates between 8am. to 5pm. Mon-Fri. The administrator could set the login times to be from 6am. to 8pm. Mon-Fri. This prevents potential malicious activity while the company is not operational.

## Account Audits
An *account audit* looks at the permissions assigned to users and helps enforce the principal of least privilege. *Privilege creep* often occurs which is when permissions are added and others which are not needed are not removed. This is why auditing is necessary to avoid these privilege bloat. 

*Attestation* is a formal process for reviewing user permissions. In an attestation process, managers formally review each user’s permissions and certify that those permissions are necessary to carry out the user’s job responsibilities.



