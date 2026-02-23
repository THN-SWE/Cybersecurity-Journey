##### Subnetting is deviding a large network into small networks 

- **In Subnetting we don't use classes we use something call CIDR value**
- **CIDR - Classless Inter Domain Routing* 
- **A CIDR value is how many network bits a ip address have.** 

eg: 
#### 192.168.10.0/24 

##### Subnet Mask : 11111111.11111111.1111111.00000000 (in binary)
- Here the CIDR value is 24 (since 24 network bits (the ones))

Now we are going to make the host bits into network bit one by one and see how they are devided into netoworks.

### 192.168.10.0/25

##### Subnet Mask : 11111111.11111111.1111111.10000000 (in binary)
number of network bits = 25 | number of host bits = 7
number of host ip address = 2 ^ 7 = 128 
Nework devided into 2

### 192.168.10.0/26

##### Subnet Mask : 11111111.11111111.1111111.11000000 (in binary)
number of network bits = 26 | number of host bits = 6
number of host ip address = 2 ^ 6 = 64 
Nework devided into 4

### 192.168.10.0/27

##### Subnet Mask : 11111111.11111111.1111111.11100000 (in binary)
number of network bits = 27 | number of host bits = 5
number of host ip address = 2 ^ 5 = 32 
Nework devided into 8

### so on.. 

# Reference 
[subnetting](https://www.youtube.com/watch?v=c6ENgy21hyI&t=909s&ab_channel=LearnTech)
