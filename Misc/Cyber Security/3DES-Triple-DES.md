
 `2024-07-25 : 23:11`
 ###### tags:
-------------
#### 3DES / triple DES

It is the successor of DES algorithm.

It is basically [[DES-Encryption-Algorithm]] but used 3 times in the equation. 

#### in 3DES

- uses 3 keys k1, k2, k3
- Each key is 56 bits => 168 bit 

##### encryptDES(decryptDES(encryptDES(p)))
p - plain text

k1 != k2 != k3 is the most common [[key-ring]].

key ring lets the implementation of 3DES also works for DES. ( when k1 = k2 = k3 )


  
#### Reference 