> The **TCP/IP model** is a framework used to visualize how data is organized and transmitted across a network

> By understanding this as a Security analyst, we can conceptualize the processes on network and can identify where exactly the disruption or security threats occur. 

- TCP/IP model has 4 layers. 
- when issues occur in the network security professionals can analyze which layers were impacted by an attack based on what processes were involved in an incident.
- This model explains:  **==The TCP/IP model explains how data created by an application on a computer is prepared and transmitted into the network for delivery.==**

![](../../Screenshots/Screenshot%202026-03-14%20122742.png)

#### 1. Network access layer (aka Data link layer)

> Getting data from your computer onto the local network using physical hardware and local addressing.

- In this layer we're dealing with: 
	- Network cards
	- cables 
	- *MAC address*
	- *frames*
	- [ARP-protocol-networking](../../Misc/ARP-protocol-networking.md)

#### 2. Internet layer (aka Network layer)

> Responsible for ensuring the delivery to the destination host.

- In this layer we're dealing with: 
	-  IP
	- [[../../Misc/ICMP]]

#### 3. Transport layer

> It ensures that data is reliably transmitted to the destination service

- In this layer we're dealing with: 
	-  Ports
	- TCP protocol
	- UDP protocol

#### 4. Application layer

> The application layer is responsible for making network requests or responding to requests.

- Application layer protocols rely on underlying layers to transfer the data across the network.

- In this layer we're dealing with: 
	-  HTTP
	- SMTP
	- SSH
	- FTP
	- DNS


#### TCP/IP model versus [OSI-Model](../../Misc/Cyber%20Security/Network%20Engineering%20-%20freecode%20camp/OSI-Model.md)

![](../../Screenshots/Screenshot%202026-03-14%20140148.png)


