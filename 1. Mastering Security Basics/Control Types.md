Control types describe the goal that the control is trying to achieve.

* **Preventive controls** attempt to prevent an incident from occurring. 
* **Detective controls** attempt to detect incidents after they have occurred. 
* **Corrective controls** attempt to restore normal operations after an incident occurs. 
* **Deterrent controls** attempt to discourage individuals from causing an incident. 
* **Compensating controls** are alternative controls used when a primary control is not feasible. 
* **Directive controls** provide instruction to individuals on how they should handle security- related situations that arise.

## Preventive Controls
Ideally, an organization will not have any security incidents, this is the primary goal of *preventive controls*.

1. **Hardening**: The process of making a system more secure than its default configuration. 
2. **Training**: Ensuring users, employees are educated about vulnerabilities and  attacks like phishing.
3. **Security Guards**: Guards help prevent and deter attacks, just by being there .
4. **Account Disablement Process**: This ensures that accounts are disabled, for example when an employee leaves the company. 
5. **Intrusion Prevention Systems**:  An IPS can block malicious traffic before reaching the network.

## Detective Controls
After an incident occur it is still important to detect and correct them. 

1. **Log Monitoring**: Firewall logs, logins. etc. By[[Logging and Monitoring| monitoring these logs]], it is possible to detect incidents.
2. **Security Information and Event Management (SIEM) Systems**: these systems detect trends and provide alerts in real time. 
3. **Security Audits**: These can examine the security posture of an organization. They can also detect past incidents.
4. **Video Surveillance and Motion Detection**: Record activity within an enclosed space. Can detect when someone entered or left a room
5. **Intrusion Detection Systems (IDS)**: These can detect malicious traffic after it enters a network. Will raise an alarm to notify IT personnel.

## Corrective Controls
They restore the confidentiality, integrity, and/or availability that was affected by the incident.

1. **Backups and System Recovery**: Backups ensure that personnel can recover lost or corrupted data. 
2. **Incident Handling Process**: Define the steps to take in response to security incidents

## Deterrent Controls

Some deterrent controls attempt to discourage potential attackers from attacking, and others attempt to discourage employees from violating a security policy.

1. **Security Guards**: Guards help prevent and deter attacks, just by being there.
2. **Warning Signs**: Warn potential intruders that the facility is monitored. 
3. **Login Banners**: Computer warning saying that attempting to use the system without permission is bad.

## Compensating Controls

Compensating controls are alternative controls used instead of a primary control. For example, an organization might require employees to use smart cards when authenticating to a system. However, it might take time for new employees to receive their smart card. To allow new employees to access the network and still maintain a high level of security, the organization might choose to implement a Time-based One-Time Password (TOTP) as a compensating control. The compensating control still provides a strong authentication solution.

## Directive Controls

Written documents that contain instructions on how individuals should handle security-related incidents that arise. 

1. **Policies, Standards, Procedures and Guidelines**: Documents used to direct actions. Policies provide a high-level goal statement for the org. Standards describe how to configure systems, applications and security controls adequately. Procedures offer guidance on achieving a goal. Guidelines offer advice on achieving goals.
2. **Change Management**: Ensures that changes do not result in unintended outages. 

> [!TIP]
> It’s important to realize that the control categories and control types are not mutually exclusive. In other words, you can describe most controls using more than one category and more than one type.