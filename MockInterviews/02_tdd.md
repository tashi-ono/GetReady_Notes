# Notes 9/27/2020

## What is Test Driven Development (TDD)?

- Philosophical approach to writing code.
- Write unit tests before writing the code
- It forces you to design your classes correctly from the start
- Use informal specifications to design your tests
  - can draw diagrams to figure out what you may want your code to do

## Unit Testing vs TDD

- Unit testing is just a type of automated testing in which you test individual units of behavior
- TDD is creating a unit test before writing your actual code

## Red-Green-Refactor

1. Method stub

   - Create stubs for class and public members
   - This stub doesn't have functionality
   - Will state
     - name
     - return value
     - parameter names and data types (Java)

2. `RED`: Create several tests that will initially fail
3. Write the code for the unit we are testing
4. `GREEN`: Debug code until all tests pass keeping in mind initial solutions don't have to be elegant at this point
5. Create additional tests to account for any missed corner cases
6. `REFACTOR` code for readability or performance efficiency

[Back to Table of Contents](https://github.com/tashi-ono/GetReady_Notes)
