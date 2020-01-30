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

# Microservices vs Monolith Architecture 

## Monolith
* Less complex, less duplication, faster
* More uniform, better for small scale 
* Cons: too much responsiblity on individual server, hard to learn for new member

## Microservice 
* More scalable
* Each task is small, making it easier to learn
* Less tight coupling
* Easier to analyze which specific funtion need to be scaled more

# Database Sharding
* Improves read/write of DB

## Important database features
* consistency
* Availability

## What is sharding?
* Divide database into sub databases
* Divide on a certain key such as user_id or location

## Problems
* Joining across shards
* What happens when it fails?

## Alternatives
* NoSQL database
* Indexing keys

## Master/Slave architecture 
* Write always goes to master, copies to slaves
* Slaves continuously read from master and copy data
* Read can be done from slaves
* When master fails, slaves decide one to takeover master
* Single point of failure 






