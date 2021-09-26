## Confused Deputy Problem

Whenever a person/agent/computer program/process or anyting whose authority is not one or is taking actions on behalf two or multiple users this situation can arise.


### Real Life Examples for Confused Deputy Problem

* Cross-site request forgeryucts 
* Clickjacking
* FTP Bounce Attack


### Cross-site request forgery

Web browesers generally use cookies to authenticate all requests transmitted by browser. An attacker can take advantage and can inject a javascript which can also submit a legit request.

Here Web Broswer is a confused deputy as its under two authority.

### Clickjacking

Hijacking users clicks and redirecting to a different website. A user  can be tricked on a website by clicking on a unwanted link.


### FTP Bounce Attack

Suppose X is a user on attacker.com and X wants to transfer a file from target.com. But, X does not have permission to transfer files from target.com. There is another machine middle-man.com who has permission to transfer files from target.com.
So, X makes a plan. He opens an FTP connection to middle-man.com. And then, instructs middle-man.com to transfer the file from target.com to attacker.com using FTP protocol. This is called 

Attacker exploits the FTP server running in passive mode, Here FTP server is the confused deputy, 

### How To prevent 

In this an unforgable token of authority is assigned to a user and the token contains a set of user access rights granted to program.


### References
* FTP Bounce Attack : https://www.thesecuritybuddy.com/vulnerabilities/what-is-ftp-bounce-attack/
* How FTP works https://afteracademy.com/blog/what-is-ftp-and-how-does-an-ftp-work
