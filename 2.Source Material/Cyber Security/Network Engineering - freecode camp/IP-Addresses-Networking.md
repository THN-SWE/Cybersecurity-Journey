
 `2024-07-23 : 20:38`
 ###### tags:
-------------

#### Structure of IP address

- An ip address is separated into 2 parts. **Network part** and **Host part**. 
- Size of a IPv4 is 32 bits. 8 bits for a segment. Each segment aka octet can represent 0-255. 

#### Subnet mask
##### 255.0.0.0 (a class a ip address's)
here:
- **255 is Network part**
- **0 is host part** 

#### Classes in IP address

##### Range - max network - max host - subnet mask

A : 10-126 126 16M 255.0.0.0

*127 ip reserved for loopback*

B: 128-191 16K 64K  255.255.0.0

C: 192-223 2M 254 255.255.255.0 

D: 224-239 RESERVED for Multicasting

E: 240-255 EXPERIMENTAL

#### Why using class C for PRIVATE  IP address 
Because class C IP address take the minimum amount of public IPs.  255.255.255.0

#### Extra

The formula to calculate the number of usable hosts is $2 ^ h −2$, where ℎ is the number of host bits (the subtraction accounts for the network and broadcast addresses)
#### Reference 