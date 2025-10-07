When discussing different network devices, it is important to remember the primary methods IPv4 uses when addressing TCP/IP traffic. 

* **Unicast**: One-to-one traffic. One host sends traffic to another host using a destination IP address. Other hosts on the network can see the packet but will ignore it since the destination IP is not theirs. 
* **Broadcast**: One-to-all traffic. One host sends traffic to all other hosts on the subnet using a broadcast address such as 255.255.255.255. Every host that receives broadcast traffic will process it. Switches pass this traffic but Routers do not.

## Switches
A *switch* connects computers and other devices to each of its physical ports. It creates internal switched connections when two computes communicate with each other. It uses a routing table to know which ports to send data. This will be used with *unicast* traffic but *broadcast* traffic is still sent to all hosts. 

If an attacker uses a protocol analyzer and it attaches to port 3, it will only be able to capture packets that are sent through this port. If two clients are using ports 1 and 4 the analyzer will not be able to capture them. For this reasons companies have been switching ***hubs*** with switches. This is because a protocol analyzer on a hub would capture all the packets and switches are more efficient anyways. 

##### Hardening Switches
These devices are the frontlines of networking and should be secure. 

* **Port Security**: Limits the computers that can connect to physical ports, At the most basic level, admins disable unused ports.
* **MAC Filtering**: The switch can be configured to block [[Basic Network Concepts#Addresses|MAC addresses]] which are not trusted or are not suing the switch. 
* **Broadcast Storm and Loop Preventions**: In some cases, a network can develop a *switching loop*. This floods the network with traffic. This can happen by connecting two ports of a switch together with a cable. To prevent this, *Rapid Spanning Tree Protocol (RSTP)* and *STP* are used. 
* **Bridge Protocol Data Unit Guard**: STP sends *Bridge Protocol Data Unit* messages in a network to detect loops. Switches exchange BPDU messages with each other using their non-edge ports. An ***edge-port*** is a switch port connected to a device. These devices should not generate BPDU messages because they will be flagged as malicious. Many switches support *BPDU guard*.  

## Routers
