There are many ways users and systems can perform authentication. These are grouped into categories known as authentication factors to better describe how they work. We will study four of them:

1. Something you know, such as a password or personal identification number (PIN) 
2. Something you have, such as a smart card, a phone, or a USB token 
3. Something you are, such as a fingerprint or other biometric identification 
4. Somewhere you are, such as your home or office

## Something You Know
These is often the least secure form of authentication, because knowledge can be stolen. If i can find a user's password I can just login as them. Because of this, a list of rules is commonly used for password authentication.

* Hash all passwords
* Use Multi Factor Authentication
* Require password to be complex; longer than eight characters, include special characters.
* Tell users to not use the same password for everything

##### Password Length & Complexity
One of the most common password requirements is the length, the longer a password the more possible possible passwords there can be, which slows down brute force attacks. Password can be longer than eight characters and still be insecure, take for example the following password: **SecurePassword123**, a brute force attack may never crack it but a dictionary attack will instantly crack it. 

##### Password Expiration/Age
A *password expiration* setting identifies when users must change their password. These days, the best practice for password security is **not** to have passwords expire. This is because users are more likely to use strong, secure passwords if they do not need to keep changing them. This advice is only true if the org uses MFA.

##### Password History and Reuse
Many users would prefer to use one password for everything, in we have a password expiration policy in place we do not want users to pick a password they have already used in the past. 

A *password history* file system remember past passwords and prevents users from reusing them. It is common for these systems to remember the last 24 passwords and prevent users from reusing them until they have used 24 new passwords.

A *minimum password age* setting makes it so users cannot change their password immediately, otherwise users would just set 24 new passwords and go back to their original password. 

##### Password Managers
A password manager (or password vault) is a single source designed to keep most of your passwords. Instead of requiring you to memorize many different passwords, you only need to remember the password to open the vault. It keeps these passwords in an encrypted format, preventing unauthorized users from seeing them.

##### Knowledge-Based Authentication
Some orgs use *knowledge-based authentication (KBA)* to verify the identify of individuals. There are two types: static KBA and  dynamic KBA

1. **Static KBA** is used to verify your identity when you have forgotten your password. What is your first dog's name. etc.
2. **Dynamic KBA** identifies people without an account. Used for high-risk transactions. The site queries public and private data sources to craft multiple choice questions only the user would know. Often these have a time constraint to avoid attackers from doing research. When was your home build? Where have you previously lived?

##### Implementing Account Lockout Policies
Accounts will typically have lockout policies which prevent users from guessing the password. Too many attempts and the account will lock the account.

* **Account Lockout Threshold**: The maximum number of times a user can enter the wrong password. Any failed attempt after this will lock the account. 
* **Account Lockout Duration**: How long the account will remain locked for. If the duration is set to 0 this means the account will be locked until its unlocked by an admin.

##### Changing Default Passwords
When installing a system of service they may include a default account username and password it is important to change these as soon as possible to prevent an attacker guessing them.

## Something You Have
Basically something you can physically hold.

##### Smart Card Authentication
