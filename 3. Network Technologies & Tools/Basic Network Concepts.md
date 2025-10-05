*Networks* carry data between computer systems. They interconnect desktop computers, servers, mobile devices, infrastructure components and anything else that needs network access.

## OSI Model
The *Open Systems Interconnections (OSI) model* is a theoretical way to describe all the different activities that happen on a network. The model consists of seven different layers.

> [!TIP]
> You can use a memory trick to remember the order of the OSI layers – make a sentence that has words starting with the seven letters of the model layers in order. My personal favorite is “Please Do Not Throw Sausage Pizza Away!”

1. **Physical**: Basic equipment of networking: Copper wires, fiber optic cables, and radio waves.
2. **Data Link**: Is where network switches reside. It formats data into data frames and routes it between systems on the local network using MAC addresses.
3. **Network**: Introduces IP addresses. Routers use IP addresses to send information between systems that are not located on the same local network. 
4. **Transport**: Provides end-to-end communication services for applications. TCP and UDP exist in this layer.
5. **Session**: Establishes, manages and terminates sessions between applications running on different devices.
6. **Presentation**: Translates data into a standard format that can be understood by the application layer and provides encryption, compression and other transformation services.
7. **Application**: Provides network services to applications, allowing them to communicate with other applications over the network. 

## Addresses
* **MAC (Media Access Control)** address is a unique, 12-digit hexadecimal identifier assigned to a device's network interface controller (NIC) for physical network communication. It's like a unique serial number for your device's network adapter, ensuring it can connect to a local network using technologies like Wi-Fi, Ethernet, or Bluetooth
* An **IPv4 address** is a unique numerical label assigned to devices on a computer network using the Internet Protocol version 4, typically displayed as four decimal numbers separated by dots (e.g., 192.0.2.1). It's a 32-bit number that uniquely identifies a device (host) within a network and consists of a network prefix and a host number. Although it provides a vast number of addresses (over 4.2 billion), the pool of available IPv4 addresses is largely depleted.
* An **IPv6 address** is a 128-bit number, longer than an IPv4 address, that serves as a unique identifier for devices on a network. It is written as eight groups of four hexadecimal digits, separated by colons (e.g., `2001:0db8:85a3:0000:0000:8a2e:0370:7334`). Leading zeros in a group can be omitted, and one or more consecutive groups of all zeros can be replaced by a single double colon (`::`) for brevity, though only once per address

## Network Protocols
Networking protocols provide the rules needed for computers to communicate with each other on a network. Some *Transmission Control Protocol/Internet Protocol (TCP/IP)* protocols, such as *TCP* and *IP*, provide basic connectivity. Other protocols, such as *Hypertext Transfer Protocol (HTTP)* and *Simple Mail Transfer Protocol (SMTP)*, support specific traffic types.

* **Transmission Control Protocol (TCP)**: Connection-oriented traffic with guaranteed delivery. Uses a three-way handshake. 
	1. SYN
	2. SYN + ACK
	3. ACK
* **User Datagram Protocol (UDP)**: Provides ***connectionless*** sessions. Unlike TCP, UDP tries its best to delivery data without using extra traffic to ensure delivery.  
* **The Internet Protocol (IP)**: Identifies hosts in a TCP/IP network and delivers traffic from one host to another using IP addresses (IPv4 and IPv6)
* **Internet Control Message Protocol (ICMP)**: Used to test basic connectivity and includes tools like ping and tracert. Due to the use of ICMP in DoS attack it is commonly blocked at firewalls and routers.  
* **Address Resolution Protocol (ARP)**: Resolves IPv4 addresses to MAC addresses. TCP/IP uses the IP address to get a packet to a destination network. It then uses the [[Basic Network Concepts#Addresses|MAC]] address to get it to the correct host. In other words, ARP is required once the packet reaches the destination subnet.
