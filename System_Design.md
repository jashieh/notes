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

