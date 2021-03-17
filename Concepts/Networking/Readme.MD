## Random Networrking Concepts 

 
 <img src="https://github.com/santojos/Distributed-Systems/blob/main/Concepts/Networking/OSI-model.png" width="800" height="550">

**Maximum Frame Size MFU** is the largest frame a network (segment) can transport. For Ethernet, this is **1518 bytes by definition.**

**Maximum Transfer Unit MTU** is MFU - 18 = 1500, The Frame has the IP packet

**Maximum Segment Size MSS** is MTU minus the IP overhead minus TCP overhead, this is 1500 - 20 (IPv4 overhead) - 20 (TCP overhead) ) = 1460 bytes.

**Round Trip Time RTT** is total time it takes for a packet to travel from source to destination and back again.


### Questions

###### Q. How can a TCP window size be allowed to be larger than the maximum size of an ethernet packet? 
###### A. https://networkengineering.stackexchange.com/questions/54107/how-can-a-tcp-window-size-be-allowed-to-be-larger-than-the-maximum-size-of-an-et
