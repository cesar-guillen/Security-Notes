There are common authentication services that allow users to get authenticated without needing to send credentials in cleartext over the network.

## Single Sign-On
*Single sign-on (SSO)* refers to a user's ability to log on once and access multiple systems without logging on again. SSO increases security because users only need to remember one password and are less likely to write them down. 

SSO requires strong authentication to be effective. If users create weak passwords, attackers might guess them, giving them access to multiple systems. Some people debate that SSO adds in risks because if an attacker can gain the user’s credentials, it provides the attacker access to multiple systems.

## LDAP
The *Lightweight Directory Access Protocol* is ac ore component of many *single-sign-on* systems. LDAP allows users and applications to retrieve information about users from the organization directory. Windows domains use this protocol in Active Directory

## SSO and a Federation
Similar to regular SSO this system tries to use the same protocol over two different networks. To do this a centralized system in this case a *federation*. A *federation* requires a federated identity management system that all members of the federation use. A federated identity links a user’s credentials from different networks or operating systems, but the federation treats it as one identity.

##### SAML
*Security Assertion Markup Language (SAML)* is an *Extensible Markup Language (XML)*-based data format used for SSO on **web browsers**. Imagine two companies that trust each other have a website, a user can login to one and would also be automatically logged on the other site. 

SAML defines three roles. 
1. **Principal**: The user logs on once. If necessary, the principal requests an identity from an identity provider.
2. **Identity provider**: And identify provider (IdP) creates, maintains and manages identity information, authentication and authorization for principals. The IdP could be any of the two networks or a third party.
3. **Service provider**: A service provider is an entity that provides services to principals. In this case it provides the websites for both networks.

## OAuth
*OAuth (Open Authorization)* is an open standard for authorization that many companies use to provide secure access to protected resources. It allows users to grant on service access to information in another service without disclosing their login credentials. 

Take for example Doodle which asks you if you want to link your account to google calendar, you would not want Doodle to know your password but you authorize this service to access and edit your calendar.

> [!REMEMBER]
> It’s easy to get confused about what OAuth does because the name is ambiguous! Remember that the “Auth” in OAuth stands for authorization, not authentication!

