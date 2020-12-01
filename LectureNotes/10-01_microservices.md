# Microservices

## Scaling the System

- In a monolith with modules A-E, module B is using critical amounts of CPU, which can potentially crash the system
- "Vertical scaling" allows us to stack more hardware on top of previous hardware (ie. Add more CPU power: 2 CPUs to 4 CPUs)
- Cons:
  - Vertical Scaling isn't dynamic
  - No way to scale back to original capacity when we don't need the extra CPUs
- "Horizontal scaling" is cloning machines to have extra capacity (ie. having several servers that all have modules A-E)
  - similar con in not being able to scale back down easily when there is less traffic to a website

## What are Microservices?

- Amazon & Netflix pioneers
- Building blocks of cloud-native applications
- Usually assigned to a single team
- Software dev architecture style that allows us to design, develop, and maintain an application by breaking it up into smaller pieces called microservices
- Easier and faster deployment to the cloud
- A micro-service
  - Single function module
  - Developed and deployed independantly (can be different language from other microservices)
  - Communicate with well-defined REST APIs (documentation) to the other modules of the over-arching application as a whole

## Inside a Microservice

1. API Gateway
   - Endpoints are defined on where you can get the JSON data you need
   - Interfaces with the user of the microservice
   - Imposes rules on how data can be accessed
2. Application Logic
   - Handles request from gateway and retrieves data from Data Store
   - Can be coded in any language that is suitable for the job
   - Formats data into JSON before sending back to gateway
3. Data Store
   - Each microservice encapsulates its own data store
   - Keeps modularity and loosely couples microservices with one another
   - Select best database technology for specific use

## Developing Microservices

- Number of microservices?
  - How many business services are available?
- Size of microservice team?
  - Amazon stipulation for team size is number of ppl that can eat 2 boxes of pizza
- Complexity of microservice should be limited
  - Do one thing well

## DevOps

- Traditionally 2 teams would handle lifecycle of an application or service

1. Development
   - Design
   - Develop
   - Test
2. Operations
   - Deploy
   - Monitor

## Challenges with Microservices

- Complex architecture
- Some services may be working in the cloud while other are still working on on-premise servers
- Since services are becoming more simpler and smaller, you may have to create more of them
- Large overhead of initial set-up
  - Therefore, monoliths may be more beneficial if running small applications where one codebase is needed
- Networking
  - Complexity moves to the external interactions of multiple services
  - Implementing best mechanism of communication between services must be considered
  - All services must communicated based on remote calls using APIs (cloud)
  - Network bandwith and latency considerations
- Monitoring
  - Collecting telemetry data - metrics, alarms, logs,
  - Large number of services in a distributed (international) and dynamic environment makes collecting data challenging
- Resiliency
  - Need to design more fault-tolerant application
  - Identify and ensure core services that my have junctions of high traffic aren't a 'single-point-of-failure'
    - Ex: Back-up servers should be available

[Back to Table of Contents](https://github.com/tashi-ono/GetReady_Notes)
