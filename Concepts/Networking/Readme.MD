## Random Networking Concepts 

 
 <img src="https://github.com/santojos/Distributed-Systems/blob/main/Concepts/Networking/OSI-model.png" width="800" height="550">

### OSI

| Layer Name    |Transfer Unit | What it does |
| ------------- | ------------- |-----------------|
| Application   | Data  | HTTP, FTP etc |
| Presentation  | Data  | Encryption! TLS etc |
| Session       | Data  |   PPTP, SOCKS |
| Transpot      | Segments | TCP, UDP |
| Network       | Packets | IP and routing | 
| Data-link | Frames |  MAC addresses and the like |
| Physical | Bits |   Electricity on a wire |
 

### The Internet protocol suite

The IP suite is much simplar then OSI model, its with less layers  

| Layer Name    |Transfer Unit | What it does |
| ------------- | ------------- |-----------------|
| Application   | Data  | HTTP, TLS, DNS, SMTP, FTP etc |
| Transpot      | Segments | TCP, UDP |
| Network       | Packets | IP (v4 and v6) | 
| Link          | Frames |  Ethernet & Wireless LAN |

* Two machines needs a physical mechanisam to sends digital data, Machine sends bits over LAN or WLAN, The speed and data is defined by bitrate and bandwidth.
* Every machine as a MAC and IP address.
* The Data is sent to the Router which forwards/sends to another network using the IP protocol
* The TCP/UDP protocol is used to send data. The Data is broken up into small packets, which are then reassembled at the destination.
* At application layer we talks about data and how to interpret that data, HTTP is an application layer protocol which talks about data


 

**Maximum Frame Size MFU** is the largest frame a network (segment) can transport. For Ethernet, this is **1518 bytes by definition.**

**Maximum Transfer Unit MTU** is MFU - 18 = 1500, The Frame has the IP packet

**Maximum Segment Size MSS** is MTU minus the IP overhead minus TCP overhead, this is 1500 - 20 (IPv4 overhead) - 20 (TCP overhead) ) = 1460 bytes.

**Round Trip Time RTT** is total time it takes for a packet to travel from source to destination and back again.


### Questions

###### Q. How can a TCP window size be allowed to be larger than the maximum size of an ethernet packet? 
###### A. https://networkengineering.stackexchange.com/questions/54107/how-can-a-tcp-window-size-be-allowed-to-be-larger-than-the-maximum-size-of-an-et


### References
Networking Fundamentals : https://tomnomnom.com/talks/networking.pdf
