# What is functional programming?
 Functional programming is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data 

## Pure functions benefits
  The code’s definitely easier to test. We don’t need to mock anything. So we can unit test pure functions with different contexts:
 * Given a parameter A → expect the function to return value B
 * Given a parameter C → expect the function to return value D
  A simple example would be a function to receive a collection of numbers and expect it to increment each element of this collection.



## Immutability

  When data is immutable, its state cannot change after it’s created. If you want to change an immutable object, you can’t. Instead, you create a new object with the new value.


## Filter
  Given a collection, we want to filter by an attribute. The filter function expects a true or false value to determine if the element should or should not be included in the result collection. Basically, if the callback expression is true, the filter function will include the element in the result collection. Otherwise, it will not   


## Map
The idea of map is to transform a collection.

The map method transforms a collection by applying a function to all of its elements and building a new collection from the returned values.  

## reference 
[reference](https://medium.com/the-renaissance-developer/concepts-of-functional-programming-in-javascript-6bc84220d2aa)