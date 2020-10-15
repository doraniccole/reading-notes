Pure Functions:

return the same result if given the same arguments
 (it is also referred as deterministic)
It does not cause any observable side effects
Examples of observable side effects include modifying a global object or a parameter passed by reference.
If our function reads external files, it’s not a pure function — the file’s contents can change.
Any function that relies on a random number generator cannot be pure.
Pure functions are stable, consistent, and predictable. Given the same parameters, pure functions will always return the same result. 

Pure functions benefits:

The code’s easier to test.
We don’t need to mock anything. So we can unit test pure functions with different contexts:
Given a parameter A → expect the function to return value B
Given a parameter C → expect the function to return value D
Immutability

Unchanging over time or unable to be changed.
Referential Transparency

pure functions + immutable data = referential transparency
Functions as first-class entities can:

refer to it from constants and variables
pass it as a parameter to other functions
return it as result from other functions
High Order Functions:

takes one or more functions as arguments, or
returns a function as its result
Filter function expects a true or false

Imperative approach

An imperative way to do it with Javascript is to:

create an empty array evenNumbers
iterate over the numbers array
push the even numbers to the evenNumbers array
Declarative approach
using smaller functions
Map

transforms a collection by applying a function to all of its elements and building a new collection from the returned values.
Reduce

The idea of reduce is to receive a function and a collection, and return a value created by combining the items.
