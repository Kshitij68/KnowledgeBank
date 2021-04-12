[Measuring Chaos - A Netflix Guide to Microservices](https://www.youtube.com/watch?v=CZ3wIuvmHeM&t=259s&ab_channel=InfoQ)

## Monolithic Architecture (Early Days)
Microservices architecture, benefits and challenges observed

What Microservices are not
HTTP/S -> Load Balancer -> Linux Host(s)
Linux Host(s) -> Apache Reverse Proxy
Tomcat and JavaWeb

This was connected to Oracle DB using JDBC

## What is a Microservice?

- Seperation of Concerns
    - Modularity and Encapsulation
- Scalability
    - Horizontal Scaling
    - Workload Partitioning
- Virtualization and Elasticity
    - Automated Operations
    - On Demand Provisioning

## Netflix Architecture
* Client Application hits the client library
* Client Library checks in the cache and returns if present
* Client Library hits request to Backend Service if not present and waits for response
* Backend Service after updating response, updates the cache

## Challenges & Solutions
##### Challenges
- Dependency
    - Intra-Service requests: 
         - Potential Network Latency
         - Potential Congestion
         - Potential Failure
         - Service might be in bad shape
         - Leads to Cascading Failure in downstream pipeline 
    - Client Libraries
        - Many clients
        - Common business logic
    - Data Persistence
    - Infrastructure
- Scale
- Variance (within the architecture)
- Change (how is it introduced)

Solutions
- Dependency
    - Intra-Service Requests
        - Fixed number of retries
        - 
###### 