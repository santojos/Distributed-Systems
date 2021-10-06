## Custom Logging Solution to Send container Logs to A Storage Server 

### DRAFT 

Putting some thoughts on how to design solution to send logs to a storage server like Elastic server.
or like how to design a system like fluendt or logstash. We need near real time logs on storage server

### Requirement :
    A java application is continuously writing to a log file, and we need to send this log file to storage server.

### Nature of logs 

* Continious and append only
* Keep on growing

### Some things to Consider
 
#### Authentication & Authorization model
* Why AuthN and AuthZ important
* What will auth and autz api contains,

#### Decisions: 
* What mechanishm would you use to send data to stoorage server Aysn vs Sync
* How to Pull data from file, Will you Polling or Receiving Events( Inofity)
* Who will rotate/truncate file
* How will program behave when the file is rotated or lost
* What will happend and How will process killed be handled
* What if the file goes very big
* What if the same program is reading multiple files
 
	
#### Reliability/Recovery 
* What if the storage service is down.
* What if storage server startes rejecting data because of threshhold
 

#### Observability:
* What will you do if data is rejected, 
* What all metrics will you Publish 
 
#### Prevent Abuse: 
* Only Valid application should send: AuthN and AuthZ
* Lot of junk data sent
* Retries / Circuit breaker
 
#### Memory Requirements 
 * How much CPU should this type of process consume 
 * How much Memory should we allocate to this process
	
### Deployment Model 
	Suppose we want to deploye it in Kubernates, what are the proces and cons of below processes
* Sidecar
* Within process
* Separate pod

