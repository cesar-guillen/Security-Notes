There are several elements involved when creatin a secure network. This includes the use of various topologies and network appliances.

## Security Zones
Most network have internet connectivity but it is rare to connect a network directly to the internet. Instead, its common to divide the network into different *Security Zones*.

* **Intranet**: An internal network people use to communicate and share content with each other.
* **Extranet**: Part of a network that can be accessed by authorized entities from outside the network. 

> [!NOTE]
> The goal of placing systems into different zones is to limit the connectivity they have to each other, which reduces the ***attack surface***.

##### Screened Subnet
A *screened subnet*, also known as a ***demilitarized zone (DMS)***, is a security zone between private networks and the internet. This servers will receive most of the attacks as they face the internet were most attackers seek to attack. 

![[Pasted image 20251024171928.png]]

In this configuration, one firewall separates the screened subnet from the Internet. The second firewall separates the screened subnet from the internal network. Each firewall includes detailed rules designed to filter traffic and protect both the internal network and public-facing servers.

##### Network Address Translation Gateway
*Network Address Translation (NAT)* is a protocol that translates public IP addresses into private IP addresses and viceversa. A *NAT Gateway* hosts NAT and provides internal clients with private IP addresses a path to the internet. Some benefits include:

* **Public IP Addresses do not need to be purchased for all clients**. A home or company network ca include multiple computers that can access the Internet from one router running NAT. 
* **NAT hides internal computers from the Internet**. Computers with private IP addresses are isolated and hidden from the Internet.

The drawback of NAT is that it is incompatible with IPsec. There can be two types of NAT:

1. **Static NAT**: uses a single public IP address in a one-to-one mapping. It maps a private IP address with a single public address.
2. **Dynamic NAT**: uses multiple public IP addresses in a one-to-many mapping. It decides which public IP address to use based on load.  
