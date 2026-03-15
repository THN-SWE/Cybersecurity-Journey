> Functions at the presentation layer involve data translation and encryption for the network.

> The **Presentation Layer** (Layer 6 in OSI) handles **how data is represented** so the application on the receiving side can understand it.

Its responsibilities include:

- **Data translation**: converting data between application format and network format
    
    - Example: converting internal text encoding to **UTF-8**
        
- **Encryption/Decryption**: making sure data is secure in transit
    
    - Example: **TLS/SSL** for HTTPS
        
- **Compression/Decompression**: reducing size to speed up transfer
    
    - Example: compressing images or text