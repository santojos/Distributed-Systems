

### Fallacies of distributed systems

One should be clear about some of the wrong assumptions we programmer/developers make about distributed systems

* The network is reliable;
* Latency is zero;
* Bandwidth is infinite;
* The network is secure;
* Topology doesn't change;
* There is one administrator;
* Transport cost is zero;
* The network is homogeneous.

Some good explanation with examples follows here -> https://pages.cs.wisc.edu/~zuyu/files/fallacies.pdf

---

### Network is Reliable

**Some challanges:**
1. Network is shared in big bad internet
2. On Hardware side : Power failures, Hardware going down, etc.. 
3. On Software Side : Message dropping over network, mesages queus going down, no backup, bugs in code and Security Threats like DDos attacks... 
4. Decentralized distribured network in which some side is not in our control for exaple .. say we integrated with a third part Payment Gateway


---

### Latency is Zero

**Latency**	: is a measure of how long it take from server to client, it exclude (Processing, serialization, de-serialization etc . It's just the time from server to client (in one direction) its all ready.).


##### Time Scale of System latencies

![Time Scale of System latencies](https://pbs.twimg.com/media/BmBr2mwCIAAhJo1?format=png&name=medium)

[Gist & Visualization of above](http://gist.github.com/f48b7279a8fde3341b159aee47fefc75 "Gist & visualization")
 

Consider below to decrese latency
* Avoid cross regional calls 
* Use CDN
* Use in memory Caching
* Create decopuled system by use asynchronous messaging 

---

### Bandwidth is infinite

---

### The network is secure

---

### Topology doesn't change

---

### There is one administrator

---

### Transport cost is zero

---
### The network is homogeneous

---
#### References

* Latency : https://www.youtube.com/watch?v=fgu5hM4CI6g&t=81s
