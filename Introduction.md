### Why?

**Achieve Parallelism
- Lots of CPUs, Memory, Disk Arms, all moving in parallel
**Able to deal with Faults 
- Run into an issue? Fine, another will take care of it. 
**Physical Reasons 
- Location 
**Safety and Security /Isolation 
-----------------------------------------------------------------------

A lot of ways systems fall apart. A few basic challenges that a DS can cause problems are: 
- Dealing concurrency 
- Partial Failure 
- Performance
## Distributed Systems Infrastructure 

- Storage 
- Communication 
- Computation 

### Fault Tolerance:

- Available systems: Prevents down time by switching the service to secondary system if in case anything goes wrong. 

- Re-convertibility: Must have save(s) of some kind if in case the service goes down to make sure progress is saved. 
	
	Note: Non-volatile storage is incredibly helpful in this case, if in case power goes off, etc. Expensive to upgrade/manage. (Disk arm **Recall 5103**)

- Replication: Management of replication copies is absolutely key. The main problem that occurs here is two replicas accidentally drift out of sync and cause fault tolerance. 

### Consistency:

Being able to see the most recent write, in case of a perfectly functioning system. An example of such system case where one of the client breaks down while replication to primary DB, the secondary DB (which does not have the most recent write) is used. 

	Strong consistency: Systems guaranteeing most recent write when
			 trying to fetch data.

 Expensive communication to maintain most recent write.

**Notes**: I believe Distributed Replicated Block Device (DRBD) is used for such cases. 

==================================================================




