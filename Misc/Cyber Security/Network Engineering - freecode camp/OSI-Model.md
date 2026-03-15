 `2024-07-20 : 17:11`
 ###### tags:
-------------



## OSI-Model

Like in Human body only if all the systems works human lives, 
In Networking all the layer of OSI model get accomplished Goal of [[Purpose-of-Networking]].

#### Structure of OSI                    `TCP/IP Structure` 

1. **[[../../Application Layer]]** 
2. **[[../../Presentation Layer]]**                             `Application`
3. **[[Session Layer]]**                                       
---- 
4. **[[Transport Layer]]**                                  `Host to Host`
5. **[[Network Layer]]**                                   `Internet`
-----
6. **[[Data link Layer]]**
7. **[[Physical Layer]]**                                  `Network Access`
---- 

#### Workflow of OSI action 

##### This top to down process is called Encapsulation - Sending data

1. **Application layer** generates data that is meant to be sent over the internet.
2. **Layer 4** then adds a header to it which includes Src Port and Dest Port. This construct is know as a **Segment**.
3. **Layer 3** then adds another header which includes Src Ip and Dest Ip addresses. This is known as a **Packet.**
4. **Layer 2** adds another header which includes Src mac address and Dest mac address. This is know as a **Frame**

##### To recieve data reciever would do the opposite. 

#### > OSI is simply a model, not strict rules. 


### Reference  
https://www.youtube.com/watch?v=LkolbURrtTs&t=70s&ab_channel=PracticalNetworking 