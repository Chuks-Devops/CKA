# Health Probes

This is what monitors your kubernetes to make sure it is in healthy all the time

3 Types of Probes
-  liveness probes

This Restart the application if it fails. 

- Readiness Probes

This makes sure that the application is running pretty well before serving the public

- Startup Probes

This is for legacy applications. Application that takes alot of time before startup up

## Types of health checks
- HTTP
- TCP
- Simple Command