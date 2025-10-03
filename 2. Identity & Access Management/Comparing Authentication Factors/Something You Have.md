Basically something you can physically hold.

##### Smart Card Authentication
Credit card sized cards that have an embedded microchip and a certificate. Users can insert this card into a smart card reader which will read all the information and do a certificate-based authentication. The requirements of a smart card are:

1. Embedded certificate
2. Public Key Infrastructure (PKI), for issuing and managing the certificates

Smart cards are often paired with another factor of authentication. A user could also be prompted to insert their password, this way an attacker cannot simply steal the card. He would also need to know the user's password.

##### Security Keys
A *security key* is an electronic device about the size of a car key. Used to authenticate to systems. 

The security key contains cryptographic information that completes the authentication process. Uses a USB connector to connect to the computers.

##### Hard Tokens
A *hard token* or hardware token, is an electronic device about the size of a car key. This device has an LED screen which displays a *one time password (OTP)* which the user will need to enter. This proves that the user in in possession of the device. 

##### Soft Tokens
A *soft token* or software token is an applications that urns on a user's phone and generates one-time passwords in the same way that hard tokens display them on their LED Screens. e.g. google authenticator.

the *HMAC-based One-Time Password (HOTP)* algorithm generate a new password when the user wants to. *Time-based One-Time Password (TOTP)* algorithm change their code based upon the current time, they change every 30-60 seconds.


> [!REMEMBER]
> 
> HOTP and TOTP are open-source standards used to create one-time-use passwords. HOTP creates a one-time-use password that does not expire until it is used, and TOTP creates a one-time password that expires after 30-60 seconds. Both can be used as software tokens for authentication.

##### SMS/Push Notifications
*SMS notifications* are used to make users enter the code that is being sent to them, this is not recommended anymore as it can be exploited by attackers, if the phone is already stolen this is not secure. 

*Push Notifications* instead are used for the user to click on them to verify things on a service or website for example by confirming their email.