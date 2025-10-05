Networks don’t automatically support all the available protocols. Instead, IT professionals identify a need based on organizational goals and enable the best protocols to meet that need.

## Data in Transit
*Data in transit* is any traffic sent over a network. Some common use cases related to transferring files are transmitting data over the network. The following list identifies several ***insecure*** protocols that should ***no longer*** be used.

* **File Transfer Protocol (FTP)**:  Uploads and downloads files to and from an FTP server. FTP transmits the data in cleartext making it easy to capture and read the data in transit.
* **Trivial File Transfer Protocol (TFTP)**: Used to transfer smaller amounts of data, such as when communicating with network devices. Commonly disabled.
* **Secure Sockets Layer (SSL)**: was the primary method used to secure HTTP traffic as HTTPS. SSL can also encrypt other types of traffic, such as SMTP and LDAP. However, SSL has been compromised and is not longer recommended.

Fortunately, there are several secure alternatives that you can use. Here are some ***secure*** alternatives for protecting data in transit:

* **Transport Layer Security (TLS)**: is the designated replacement for SSL. Used in HTTPs and many other secure protocols
* **Internet Protocol Security (IPsec)**: is used to encrypt IP traffic
* **Secure Shell (SSH)**: encrypts traffic in transit and be used to encrypt other protocols such as FTP. *Secure Copy (SCP)* is based on SSH and is used to securely download files over a network.
* **Secure File Transfer Protocol (SFTP)**: A secure implementation of FTP. It is an extension of SSH. SFTP transmits data using TCP port 22.
* **File Transfer Protocol Secure (FTPS)**: is another secure implementation of FTP. Uses TLS to encrypt FTP traffic.

> [!REMEMBER]
> Secure Shell (SSH) encrypts traffic over TCP port 22 and is used to transfer encrypted files over a network. Transport Layer Security (TLS) is a replacement for SSL and is used to encrypt many different protocols, including browser-based connections using HTTPS. Secure FTP (SFTP) uses SSH to encrypt traffic. FTP Secure (FTPS) uses TLS to encrypt traffic.

## Email and Web
Email and web traffic are some of the most common ways that people use the internet today. They were built without having security in mind, but secure alternatives have been built which introduce encryption. The following list shows common protocols alongside their secure counterpart which uses TLS to encrypt plaintext data.

| Protocol                          . | Port               . | Secure Version                                 . | Port               . |
| ----------------------------------- | -------------------- | ------------------------------------------------ | -------------------- |
| SMTP                                | 25                   | SMTPS                                            | 587                  |
| POP3                                | 110                  | POP3 (Same name)                                 | 995                  |
| IMAP                                | 143                  | IMAP (Same name)                                 | 993                  |
| HTTP                                | 80                   | HTTPS                                            | 443                  |

##### Enhancing Email Security
Securing email is a complex task and there are controls other than encryption.

* **Sender Policy Framework (SPF)**: Uses DNS records to define which IP addresses are authorized to send emails on behalf of a domain.
* **DomainKeys Identified Mails (DKIM)**: Uses public key cryptography to sign and verify an email's domain and context.
* **Domain-based Message Authentication, Reporting and Conformance (DMARC)**: built on top of *SPF* and *DKIM* by allowing domain owner to set policies for how to handle emails that fail authentications checks and providing reporting and monitor mechanisms. 
* **Email gateways**: network devices or software applications that act as a barrier between an organization’s internal email system and the external internet, filtering incoming and outgoing emails for spam, malware, and other types of threats.

## Active Directory 
The Lightweight Directory Access Protocol (LDAP) specifies the formats and methods used to query directories, such as Microsoft AD DS. LDAP uses TCP port 389. LDAP Secure (LDAPS) encrypts data with TLS using TCP port 636.

## Voice and Video 

