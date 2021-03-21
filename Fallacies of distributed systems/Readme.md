

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


#### Network is Reliable


#### Latency is Zero

**Latency**	: is a measure of how long it take from server to client, it exclude (Processing, serialization, de-serialization etc . It's just the time from server to client (in one direction) its all ready.).


##### Time Scale of System latencies

![Time Scale of System latencies] (https://twitter.com/PieCalculus/status/459485747842523136/photo/1)

[gist]http://gist.github.com/f48b7279a8fde3341b159aee47fefc75[/gist]

<script src="https://gist.github.com/santojos/f48b7279a8fde3341b159aee47fefc75.js"></script>
 

Consider below to decrese latency
* Avoid cross regional calls 
* Use CDN
* Use in memory Caching
* Create decopuled system by use asynchronous messaging 



#### References

* Latency : https://www.youtube.com/watch?v=fgu5hM4CI6g&t=81s
