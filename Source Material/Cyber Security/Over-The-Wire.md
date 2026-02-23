
 `2024-07-23 : 22:22`
 ###### tags:
-------------

#### Passwords

- [[Level-Bandit-Passwords]]

#### Linux Commands 

[[Linux/Linux-Commands]]

## Levels 

#### Bandits

2. Using `./-` to read the file `-`. 
5. `find ./ -type f -size 1033c`
6. ` find / -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null` 2>/dev/null is to point the error outputs to a temp file
7.  `grep -A 1 "millionth" data.txt `
8. `sort data.txt | uniq -u`
9. `strings | grep "=="`
10.  `base64 -d data.txt`
11.  `tr 'A-Za-z' 'N-ZA-Mn-za-m' < data.txt`
12.  holy process. Hexdump. Magic number - file format. renaming, decompressing. gzip, bzip2.
13. `ssh -i ~/.ssh/id_rsa bandit14@bandit.labs.overthewire.org 
     `-p 2220` 
    cp ssh key. key based ssh. 
14. `nc localhost 30000 < /etc/bandit_pass/bandit14`
15. connected to ssl/tls server using `openssl s_client -connect localhost:30001`  
16. nmap `-sV` service version scan  lets us do a service/version detection scan.
	- `nmap -sV localhost -p 31000-32000` 
	- port 31790 is the one 
17. ` ssh -i .ssh/bandit17.private bandit17@bandit.labs.overthewire.org -p 2220`
18. 


 