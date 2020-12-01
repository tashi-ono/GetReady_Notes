# Mock Interview Questions

## Interviewing Guidelines

1. Baseline
   - What is your baseline knowledge of a concept?
2. Stretch
   - Where do you start to get into uncharted territory and have gaps in your baseline knowledge?
3. Help
   - Where do you need help? Don't be afraid to step up and ask for help!

## Tips

- Be confident in your own skills
- Even if you don't know the answer, use what you do know to give your problem-solving techniques for starting to tackle the problem

## What is Imperative Programming?

- Style of building programs that expresses commands for the computer to perform, changing that program's state
- In other words, you specifiy how to do something, not just desired outcome

  - provides steps to solve a problem (algorithms)
  - small problems easily solved using procedural implementation, however...
    - harder to scale with larger problems
    - "tightly coupled" behaviors are hard to modify down the road
    - harder to debug

- Types of Imperative Programming

  - parallel processing
  - procedural (structured) programming
  - OOP

  - Characteristics:

  - variables, pointers, and stored procedures are common
  - data is mutable
  - Inheritance is common and used as example of reusable, clean code

### OOP

- large problems are easily scaled with this paradigm as humans tend to think in terms of using objects in real life
- use objects to package information for our code

## What is Declarative Programming

- Style of building programs that uses functions to transform data, but does not have state of its own, nor does it mutate the data
- In other words, you declare WHAT you want to happen NOT HOW it's implemented
- Types of Declarative Programming:
  - functional programming
  - logic programming
  - database processing
- Characteristics:

  - relies on functions (similar to mathematical computing)
  - No loops or conditional statements
  - Data is considered immutable values.
  - Though you can perform filters or operations on the data as a whole
  - Doesn't change environment outside of the function.
  - More testable and reliable code

## What is an Interpreted vs Compiled Language?

- Interpreted language like JavaScript is read line by line
- Compiled language like Java is byte code under the hood

## JavaScript Questions

### What is a closure?

- In JavaScript, a closure is a function that has access to variables in its outer environment, but only its direct outer environment
- This direct outer environment is usually referred to its lexical scope, or the environment in which the function was created

### 2 Programming Paradigms in JS?

1. Object-Oriented (form of imperative or procedural programming)
2. Functional (type of declarative programming)

### Why is JS considered 'multi-paradigm"?

- JS Supports:
  - OOP (Java is purely this)
    - prototypal inheritance
  - functional programming (SQL is purely this)

### What is OOP?

- Programming paradigm in which we use objects to model real-life objects in order to problem solve
- OOP uses:
  - objects
  - classes (which are prototypes in disguise for JS)
  - prototypes

## Pros and Cons of Functional vs Object-Oriented Programming

#### OOP

- Use when there are many things and few or fixed number of operations

| Pros                                          | Cons                                 |
| --------------------------------------------- | ------------------------------------ |
| Can model real-life problems as objects       | Tightly-coupled inheritance          |
| Enterprise ready                              | Harder to debug due to sharing state |
| Loosely-coupled composition                   |                                      |
| Reusable code due to inheritance              |                                      |
| Provides data encapsulaton (good for backend) |                                      |

- Easier to problem solve with since humans tend to think in concrete objects (data structures) rather than abstract computations
- Considered more enterprise ready and reusable due to the ability of using inheritance
- However, tightly-coupled code that inherits from parent classes are harder to debug because you could have issues in `delegate classes` that would be hard to track
- Objects are also nice because they encapsulate data, which protects it from unwanted external access or usage
- Good for backend data encapsulation

#### Functional Programming

- Use when there are few or fixed number of things with more operations

| Pros                                     | Cons                                 |
| ---------------------------------------- | ------------------------------------ |
| Loosely-coupled                          | Pure functions (cannot store state ) |
| Easier to scale (b/c loose coupling)     |                                      |
| Avoids side-effects (b/c loose coupling) |                                      |
| Simple composition                       |                                      |
| Good for frontend functionality          |                                      |

- Since functions only affect behavior, they do not store state like objects can
- Easier to scale because functions don't rely on tightly-coupled inheritance and can be added to without having to mess with your original code
- Good for frontend functionality

## Why should we favor object composition over classical inheritance?

- Object composition allows you to pick and choose what properties and methods are inherited from prototypes
- Classical inheritance makes you inherit everything from a parent class, therefore possibly duplicating code you don't need in your subclasses

## 4 Pillars of OOP

1. Abstraction
   - Abstraction is basically an interface
   - Only showing pertinent, functional parts of your code and hiding implementation code
   - Hiding implementation code makes the overall program easier to understand for other developers
   - For example, abstraction is like importing react into a React project without showing everything that is under the hood.
2. Polymorphism

   - The ability of a piece of code, like an object, to have many forms
   - In other words, an object can have a base composition, but its methods may be implemented differently depending on what arguments are passed into it (static polymorphism) or what kind of subclass is inheriting it (dynamic polymorphism).
   - For example a beer class would have a certainp properties as well as a `pourBeerIntoGlass()` method. That method would be implemented differently depend on if it is inherited by the Stout class or the IPA class. In the IPA class, that pour method would be implemented with CO2, whereas the Stout class would implement the pour method with nitrogen.

     #### Explain the 2 kinds of Polymorphism?

     1. Static (compile time) aka function overloading
     2. Dynamic (runtime) aka method overriding

3. Inheritance

- A child class inherits properties and methods from a parent class

4. Encapsulation

- A piece of code is enclosed (like how objects are enclosed with curly brackets) to protect the scope of the data consealed within
- Great for backend code as it is protected and must be accessed or modified using getter/setter methods

## 5 SOLID Principles of OOP

1. Single Reponsibility (SRP)

   - A piece of code (class, function, etc), must have only 1 reason to change, or one dependancy
   - In other words meaning only one thing can break this piece of code, which will not affect the rest of the program
   - This makes the code more `cohesive` and succinct w/ loose coupling, allowing it to be easily debugged without having to change other code blocks
   - Example of a bad SRP program that allows you to checkout library books, but has too many dependancies of:
     - Storing user's contact info
     - Recording their checkouts
     - Charge late fees

2. Open/Close

   - Open for extension, closed for modification
   - Meaning you can add to a piece of code, but you can't change its base composition
   - `if` and `switch` statements are violations of the 'Open/Close' principle because if you wanted to add to the code, you would have to modify the statements
   - Instead turn switch statements into classes if possible
   - Ex: An abstract class shouldn't need to be modified as class instances should be made to extend upon other properties or methods
     - This allows the abstract class to be more modular and prevents us from having to backtrack on code we've already written

3. Liskov Substitution

   - Expounds upon the Open/Close Principle
   - aka Classical Inheritance
   - I believe this is more in regards to classical inheritance where the parent class is a template, rather than an instance like Javascript's prototypical inheritance
   - A child class can be substituted for its parent class and it should still be able to work since it is just an extension of the parent.
   - If the child class has to use other methods that are not an extension, but entirely different from what is in parent class, then this demonstrates composition instead of inheritance, therefore violating Liskov Substitution
   - In classical inheritance, we may want the subclass instance to be a perfect clone of the superclass reference because of tightly coupled code that relies on the superclass

4. Interface Segregation

   - Is abstraction (interface), but mostly about composition over inheritance
   - Make interface as concise and specific as possible
   - Technically in JS, there is no `interface` keyword, but we can think of class methods as interfaces because they allow us to interact with our object
   - In other words, we need to use 'composition' to create more specific methods for subclasses rather than using inheritance to take on all, including unnecessary methods from a parent class

5. Dependancy Inversion
   - Use an abstraction (interface extension? ) as an intermediary between high-level and lower-level software components or modules in order to decouple them or remove dependancies between them.
   - Think of an Adapter pattern
     - Use an intermediary API to act as an adapter between your base code and a 3rd party API
     - This allows us to keep our base code the same so that we don't have to continually change it according to how it needs to be implemented.
     - This also makes our base code more reusable and polymorphic
   - Code to abstractions not to concretion
   - Code against interfaces, not implementation
   - Java code example of other companies being able to change underlying code according to the implementation they needed, which made the code less reusable

[Back to Table of Contents](https://github.com/tashi-ono/GetReady_Notes)
