## CAP Theorem


#### How is CAP Interpreted

**Consistency**: A certain read must contain the most recently written data.

**Availability**: The system must respond with data (if available), It must be up all the time

**Partition Tolerance**: The system can function with partitions, i.e. the data is stored across multiple nodes. A network failure that splits the processing nodes into 2 groups which cannot talk to each other, then the processing should continue in both subgroups.

CAP theroem states that _one can only choose 2 out of the above 3 in a data store._

#### The Paradox
CAP theorem say pick two from **CAP**
 
 ▪️ **Lets Pick CP**
- [x] Consistent
- [x] Partition Tolerant

  An Unavilalbe data store cannot be an option, so can not choose Consistent and Partition tolerant.
 
 ▪️ **Lets Pick CA**
- [x] Consistent
- [x] Available
 
  No partition means single node, does not make sense in distributed system


▪️ **Lets Pick AP**
- [x] Available
- [x] Partition Tolerant
  
  We might get inconsistent stale data instead of no data.
  
 _Pratically two of the three combinations does not hold up._

 
#### What makes sense

**CP** looses availability only when there is a network partition, **CA** are non partition tolerent and in case there's a partition they loose availability, which means **CP** and **CA** are identical. Which furthur means in the event of a partition, what should the system give up, C or A?
 
Also consider that to be a **higly available system**, a distributed system must replicate data and as soon as data starts replicating ther arises _a tradeoff between consistency and latency._

#### PACELC Theroem

PACELC is an extension of CAP Theorem. If there is a **Partition failure**, prioritize between **Consistency** or **Availability**, **Else** prioritize **Consistency** or **Latency**.

##### PACELC has two parts

* PAC: if there is a partition failure, there's a trade off availability and consistency, hence prioritize Availability or Consistency
* ELC: Else if the system is running normally (_in the absence of partitions_), there's a trade off of latency (L) and consistency (C), hence prioritize Latency or Consistency.

#### How PACELC fits some DB Systems

| Command | Data Store |
| --- | --- |
| PA/EL | Cassandra, DynamoDB, CosmosDB |
| PC/EC | MySQL   |
| PA/EC | MongoDB |
| PC/EL | PNUTS        |
|      | Elastic Serach  |
|      | Redis |
|      | Zookeeper |
|      | HBase |


#### References

* https://www.cs.umd.edu/~abadi/papers/abadi-pacelc.pdf
* http://dbmsmusings.blogspot.com/2010/04/problems-with-cap-and-yahoos-little.html
* https://cacm.acm.org/blogs/blog-cacm/83396-errors-in-database-systems-eventual-consistency-and-the-cap-theorem/fulltext
* https://medium.baqend.com/nosql-databases-a-survey-and-decision-guidance-ea7823a822d

