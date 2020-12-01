# Notes 10/7/2020

## What are design patterns?

- Tried and true templates of ways to solve particular problems
- Example: Adapter Pattern

#### What is a Facade Pattern?

- front-facing interface used as a facade to hide more complex underlying or structural code

#### What is a DAO Pattern?

- Data Access Object
- Provides abstract interface to a database, without exposing details of the database (intermediary between application and database)
- In other words, it separates data access (in terms of using data types or domain-specific objects) from a database schema (???)

## What is MVC?

- Architectural pattern that separates an application into 3 components
  1. Model
     - handles incoming/outgoing data from database and molds them into the format we want
  2. View
     - UI components that renders data
  3. Controller
     - Interface between model and view
     - All the logic that holds our CRUD operations

## What are the 3 components all Programs should have?

- 1st tier: Frontend server
- 2nd tier: Application
- 3rd tier: Database (data store)

## What is HTTP?

- Hyper Text Transfer Protocol
  - Literally means a procedure in which we can transfer information through the web
  - Or how clients can communicate to servers using HTTP requests and responses
- HTTP request/response cycle
  - Client (browser) uses the HTTP to request data from the server
  - The server receives the request and runs an application to process it
  - Then the server returns the HTTP response to the client
  - Finally the client receives the response and renders it

## What is an API?

- Application Programming Interface
  - Literally means a way to interface with a program
  - It defines what calls or requests can be made to it and how they are made in order to extract information or functionality from that program
  - This shows the abstraction principle of OOP because you are only shown parts of a program that allow you to interact with it, without having to look at implementation code

## What is CRUD?

- Create, Read, Update, Delete
- These are the 4 functionalities we want built into our APIs
- Usually implemented by our controller

## What is a Monolith?

- Monolith in plain English: an artifact made of only one massive structure

- Single-tiered, server-side software application in which the user interface and data access code are combined into a single program from a single source.
- These allow you to perform tasks end-to-end
- Think of a mainframe computer that does heavy-duty, bulk data processing (server)
- Usually lack modularity
- Sometimes 'legacy' or outdated code that can be chopped up into microservices
- Initially, easy to develop, deploy, and manage until you have to continue adding functionalities that can convolute the code's readability
  - More code also makes deployment more difficult to handle as you would have to shut down the whole program first
- All components or functionalities within a monolith rely on the same codebase, therefore any changes to your code could potentially affect other components
- Limited to the language/framework it was originally created in

## What are Microservices?

- Software architecture that allows a program to be divied up into smaller applications
- Every app function is broken down into its own service package
- Each package or container communicates via APIs
- Since each microservice is its own entity, it can be written in any language/framework
- Each microservice can be iterated over independantly so that any changes/upgrades can be tested in a separate environment before deploying through DevOps pipeline, while the old version is still in service
- Also if a microservice fails, it doesn't affect the other microservices
- Each can be scaled independantly according to load
- Allows for modularity
- Loose coupling
- Easier debugging and deployment

[Back to Table of Contents](https://github.com/tashi-ono/GetReady_Notes)
