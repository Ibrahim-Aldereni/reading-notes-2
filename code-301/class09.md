# **Functional Programming Concepts:**

- **What is functional programming?**

  Functional programming is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data.(1)

- **What is a pure function and how do we know if something is a pure function?**

  Pure function will return the same result if given the same arguments, and It does not cause any observable side effects. (1)

- **What are the benefits of a pure function?**

  - Pure functions are stable, consistent, and predictable.
  - The code’s easier to test.(1)

- **What is immutability?**

  It means that that data state cannot change after it’s created.

- **What is Referential transparency?**

  Like a function if it's consistently yields the same result for the same input.

  > pure functions + immutable data = referential transparency (1)

# **Functional Programming Concepts:**

- **What is a module?**

  It's a javascript file that can be exported.

- **What does the word ‘require’ do?**

  To import other module in other file.

- **How do we bring another module into the file the we are working in?**

  Using require method `require(MODULE PATH HERE)`

- **What do we have to do to make a module available?**

  We need to export it using `module.exports = THE NAME OF THE DATA I WANT IT TO BE AVALIBALE`
  and the `require()` that module.

---

## Things I want to know more about:

- How can I determine if the data is immutable?
- How can I use ES6 with modules?

## Sources:

- (1) [Concepts of Functional Programming in Javascript](https://medium.com/the-renaissance-developer/concepts-of-functional-programming-in-javascript-6bc84220d2aa)

- (2) [Node JS Tutorial for Beginners](https://www.youtube.com/watch?v=xHLd36QoS4k)

[Back to home page](../README.md)
