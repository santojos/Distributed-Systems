## CAP Theorem


#### How is CAP Interpreted

**Consistency**: A certain read must contain the most recently written data.

**Availability**: The system must respond with data (if available)

**Partition Tolerance**: The system can function with partitions, i.e. the data is stored across multiple nodes.

CAP theroem states that _one can only choose only 2 out of the above 3 in a data store._


#### The Paradox
CAP theorem say pick two from **CAP**
 

 ▪️ **Lets Pick CP**
- [x] Consistent
- [x] Partition Tolerant

  An Unavilalbe data store cannot be an option, so can not choose Consistent and Partition tolerant.
 
 ▪️ **Lets Pick CA**
- [x] Consistent
- [x] Available

No partition means single node 


▪️ **Lets Pick AP**
- [x] Available
- [x] Partition Tolerant

We might get inconsistent data

Pratically two of the three combinations does not hold up.


#### PACELC Theroem


#### The PACELC Theorem and how various data stores fit/

#### References

https://www.cs.umd.edu/~abadi/papers/abadi-pacelc.pdf
