- IPS is an application that monitors system for any malicious and unlike [Intrusion Detection System](Intrusion%20Detection%20System.md) IPS takes action to stop it. 
- It does the same thing as a IDS but IPS would also block specific sender or drops network packets that seems suspect. 

- Here the IPS is placed after the firewall so that it filters out unwanted traffic reducing noise and false positives. 
- **Small doubt : Why the IPS isn't placed after the Firewall and before the router so that any malicious traffic won't reach the router.. ?** 

![](Screenshots/Screenshot%202026-03-23%20183147.png)

---
#### Limitations 

- Potential limitation is that it is **Inline** : if it breaks, the connection between private network and the Internet breaks. 
- Another one is If it gets False positives it might drop any legitimate traffic as well. 