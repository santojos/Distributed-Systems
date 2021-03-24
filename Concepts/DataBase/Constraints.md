
### Traditional RDBS
---

Early traditional daabases guarantees below properties. ACID properties provide correctnetss anc consistency.


### Transaction
  Is a smallect logical unit of work which access or modifies Database content. ACID properties are followed by transections.

#### Atomicity (A)
  A transaction must be "all or nothing". Either it should run to completion or should not run, If fails it should be rollbacked otherwisse committed. No mid way.

#### Consistency (C) 
  The transection should take the Databae from one consistent state to other consistent state
 
#### Isolation (I)
   Multiple transaction can run in parallel and should be isolated from each other. The result of all concurrent transaction should be same as if they ran in a sequence.
   
#### Durability (D)
  Once a transaction is complete the results should be persisted and never lost
  
### Isolatin level and concurrency Control
  
 
