- IDS is an application that monitors the system activity and alerts on possible intrusions. 
- IDS alerts administrators *based on the signature of malicious traffic*.
- It is configured to identify the patterns of knows attacks and it could also recognize malicious activity. 
- It sends an alert to the network admin who can then review and take action. 
---
- Limitation of IDS is that it can't stop a possible attack but only alerts. 
- And IDS only knows about known/ obvious attack anomalies. If any new sophisticated attack happen it might not identify it. 
---
- Here we placed the IDS behind the Firewall  and before entering the LAN. 
- which allows the IDS to analyze the data streams filtered out by the firewall. 
- It reduces noise in IDS alerts. (**False positives**)

![](Screenshots/Screenshot%202026-03-23%20181832.png)
