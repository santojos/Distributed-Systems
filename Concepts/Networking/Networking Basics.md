
### Networking Basics


#### MAC Address : Data Layer

* Machines have Network interface Card which has Media Access Control (MAC) address
* MAC addresses look like this: 50:46:5d:54:94:23
* Data is sent as frame and each frame has scource and destinations address
* Machines Get to Know the MAC address of other machines using ARP ( Address Resoultution Protocol ). They cache ARP for future use
* ff:ff:ff:ff:ff:ff is a special broadcast MAC adress

#### Hub/Switches 
 
* Generally machines are connected to Hub/Switches
* Hub is dumb and forwards the requests to all machines 
* Hub is slow (10Mbit, 100Mbit)
* Switches are smarter and have cache, They remember MAc address
* Switches are faster then Hub (10Gbit)
 

#### IP Address

* Each machine has an IP address
* Is of type 192.168.1.1
* Has two parts : Network Id and Host Id. For example 192.168.10.11, The first three octets (192.168.10.) is Network and 11 is the machine in the netwoek.
* Divided into A, B, and C. Classes D and E exists but not used
*

| IP Address Class  | Subnet Mask  | Octet |  Network | Hosts | 
| ----------------- | ------------ | ------- | --------- |-----| 
| A    | 255.0.0.0 | 0-127  |  126 networks | 17 million hosts per network. |
| B    | 255.255.0.0 | 128-191  |  16,000 networks | 65,000 hosts per network |
| C    | 255.255.255.0 | 192-223   |  2 million networks | 254 hosts per network  |
| D    | No subnet mask |  224 to 239 |  |
| E    | No Subnet mask |  240 to 255 | | 


#### Subnet
* Is a smaller network within a big network 
* Each machine has IP and subnet Mask

#### Subnet Mask
* It looks like 255.255.255.0. Together with IP address, it decide which subnet a machine belongs to.
* Subnet Mask of 255.255.255.0 


#### CIDR Notation
* Is basciaclly a shortcut for specifing IP and subnet which looks long
* For example this can be represented as 10.0.0.1/255.255.255.0  10.0.0.1/24
* It's the number of one's in the subnet masek

#### Router
* Has more then one IP per sub network ( per subnet)
* Has more then one network interface ( MAC Address)  
* Router is connected to multiple subnets

#### How Router Works
* Router is connected to all the subnets

##### Machines

| Machine  | MAC   | IP    |      Subnet Mask            |
|----------|-------|-------|------------------- |
|   A      | aa:aa:aa:aa:aa:aa | 192.168.0.1        | 255.255.255.0 |
|   B      | bb:bb:bb:bb:bb:bb | 192.168.1.1        | 255.255.255.0 |

##### Router

| MAC                  |    IP    |      Subnet Mask            |
|----------------------|--------------|------------------- |
|   cc:cc:cc:cc:cc:cc  | 192.168.0.254 | 255.255.255.0 |
|   dd:dd:dd:dd:dd:dd  | 192.168.1.254 | 255.255.255.0 |

* Machine A does not know the MAC address of Machine B, but knows the IP
* Machine A sends the data to Router's default gateway with Macines B IP and Routers MAC address
* Router as is connected to all the networks knows the MAC address of machine B, so its modifes the source and destinations MAC
 


### References
* https://www.youtube.com/watch?v=9uebakqWlB0&t=356s
