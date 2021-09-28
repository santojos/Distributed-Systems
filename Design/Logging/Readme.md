## Custom Logging Solution to Send container Logs to A Storage Server 

### DRAFT 

Putting some thoughts on how to design solution to send logs to a storage server like Elastic server.
or like how to design a system like fluendt or logstash.


### Nature of logs 

* Continious and append only
* Keep on growing


### Components 

* **Logrotate** that should stop logs from growning, should rotate logs if they go beyond a threashold. Rotation can be size or time based
* **Log Reader** A program that read logs from file and send to storage.

#### Log Reader

