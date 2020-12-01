# RESTful API

### What is an interface?

- A way for a user to interact with an object
- Public-facing functionality that we can interact with
- Like creating a stand-alone function that a subclass can call upon as a way to compose what additional methods it can have that werern't originally inherited from the parent class
  - In other words, allowing us to implement a version of polymorphism

### What is REST

- Representational State Transfer
  - Objects have ID, State, and Behavior
  - REST APIs send the state of an object through its interface

### Guiding Principles of REST

1. Client-server
2. Stateless
3. Cacheable
4. Uniform Interface
5. Layered System
6. Code on Demand

### What is a Client-Server

- Clients request data from a server
  - servers can also be clients that need to request data from another server
- Separating clients from servers allows the client to be scalable as you can have different kinds of clients (desktop or mobile, etc), but still use the same server

### RESTful API is Stateless

- Does not hold state
- Session state is kept entirely on the client
- Each request from client to server must contain all the info needed to understand the request
- cannot take advantage of state stored on server

### What is a Cache?

- Data frequently requested for are saved in the cache as living memory to speed up requests since the cache can be accessed instead of the database
- Threshold for requests that decides when a piece of data is cached is determined by the programmer.
- The cache lives outside the layered system

### What is a Layered System?

- The sequential procedure of a browser request being sent to a load balancer, that gets funneled to a server, then goes to retrieve data from a database

#### What makes a server crash?

- Too many requests at one time (rush hour traffic) to one server
- Resolve by scaling up with more server machines
- Load Balancers allow us to funnel traffic to the servers so there is never an overload of requests to one server
- All the servers will be hooked up to the same main database to ensure all servers have access to all data, therefore being able to scale on the number of servers needed or not needed

### Uniform Interface (???)

- What is a Service-Level Agreement (SLA)???
- By applying the software engineering principle of generality to the component interface, the overall system architecture is simplified and the visibility of interactions is improved. In order to obtain a uniform interface, multiple architectural constraints are needed to guide the behavior of components. REST is defined by four interface constraints: identification of resources; manipulation of resources through representations; self-descriptive messages; and, hypermedia as the engine of application state.

### Code on Demand

- REST allows client functionality to be extended by downloading and executing code in the form of applets or scripts.
  - This simplifies clients by reducing the number of features required to be pre-implemented.
- Example is instead of downloading Bootstrap to your machine, you can copy and paste code to add Bootstrap to your html file

### URI

- uniform resource identifier
  - The base address of a website
- URL is uniform resource locator
  - Will use the base address, then have additional info to call a specific resource

### Protocols

- SMTP
- FTP
- UDP
- HTTP: HyperText Protocol
  - Get
  - Post: creating data
  - Head: Get size or meta data
  - Put: updating data
  - Connect: test to connect
  - Options
  - Trace

#### Idempotency

- No matter how many times you call an action, it will only execute once
- Deleting a file is an idempotent action because you can only delete a file once

### CRUD

- Create
- Read
- Update
- Delete

### HTTP Status Codes

- 1xx Informational (100 continue)
- 2xx Success (200 ok)
- 3xx redirection (301 moved permanently)
- 4xx client error (400 bad request)
- 5xx server error (500 internal server error)

### WEB Sockets

- direct communication from browser to server
- less overhead (no continuous requesting ???) than HTTP requests

### Servlets

### ORM

### IoC

- Inversion of Control
- React.js
  - opinionated library on how it should be implemented

### Dependancy Injection (DI)

- design pattern
