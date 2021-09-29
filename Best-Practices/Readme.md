## Best Practices



### The Twelve-Factor App

https://12factor.net

Its a methodology for building distributed systems applications 

1. **Code base** : Single  code base in a repo that powers stage,test prod and other env, Also in case of Web App, It should power all kind of devices.

2. **Dependencies** : Explicitly declare and isolate all the dependencies. 

3. **Configuration** : There should be a strict sepration between code and configuration. Config should never be stored in code.

4. **Backing Services** : 
Treat back-end services as attached resources to be accessed with a URL or other locator stored in config.

5. **Build, Release, Run** :
Strictly separate build and run stages.

6. **Processes** :
Execute the app as one or more stateless processes. Data that must be persistent should be stored in a stateful backing service.

7. **Port binding** :
Use port binding to export services.

8. **Concurrency** :
Scale out apps horizontally, not vertically. 

9. **Disposability** :
Use fast startups and graceful shutdowns to maximize robustness.

10. **Parity** :
Facilitate continuous deployment by ensuring that development, staging, and production environments are as similar as possible.

11. **Logs** : Treat logs as event streams. Logs should not be concerned with routing or storing the app’s output.

12. Admin processes
 


### Container Best Practices
   http://docs.projectatomic.io/container-best-practices/
