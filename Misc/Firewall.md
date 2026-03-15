**A network security device which monitors the network and restrict specific incoming and outgoing network traffic.** 

- There are two types - **Physical** and Firewall as a **software** runs on  device like *windows defender*.  
- **Cloud based firewall** is another type.

#### Stateful and Stateless Firewall  and NGFW

- Any firewall should fall into any of this 2 categories. 
- **Stateful** - A class of firewall that keeps track of information passing through it and proactively filters out threat. 
- **Stateless** -   A class of firewall that operates based on predefined rules and does not keep track of information from data packets. 
- **Next Gen firewall** - Deep packet inspection, intrusion protection, Threat intelligence.  

![](../Screenshots/Screenshot%202026-03-12%20185726.png)
  Dam ! why are physical ones are so expensive ? 

#### What is the difference Physical vs Software ? 
- Unlike software firewall Physical firewall stops threats even before it reaches your device. 
- Companies deploy devices like **Fortinet FortiGate** or **Cisco ASA**
- ==Hardware firewall has its limits== 
	- malware already running on a PC
	- a malicious program sending allowed traffic (like HTTPS)
	- internal lateral movement inside the network
- A Wifi router from your home network is actually a hardware firewall. 
#### Which one is more secure ? 
- Both together : **Defense in Depth** from [5. OWASP Security Principals](3.%20Google%20Professional%20Cyber%20Security%20course/1.%20Fundamentals/5.%20OWASP%20Security%20Principals.md) remeber ! 
- Both has their strength and weaknesses. 


