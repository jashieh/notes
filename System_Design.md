# Horizontal vs Vertical Scaling

## Horizontal
* More machines
* Needs load balacing
* Resilient (multiple servers)
* data inconsistency
* scales well with users

## Vertical
* Bigger machine
* Single point of failure
* Consistent
* Fast interprocess communication 
* Hardware limit

# Load Balancer 


## What is load balancing?
* Evenly distributing load across all servers.

## Possible solutions
* Do it by random using hash, hashKey % serverNums (not a good approach)

### Consistent Hashing
* Have multiple hash functions, splitting the load between servers evenly
* Virtual servers make it less likely to load all on 1 server.

## Message / Task Queue
* Rabbit MQ, Zero MQ
* Store a list of tasks needed to be completed in DB, have a notifier that pings the server
every so often to see if tasks are complete (heart-beat)
* Use consistent hashing to prevent duplicate requests. When server goes down, requests will be sent to the 
same server.

