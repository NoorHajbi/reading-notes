# Readings: FUNCTIONAL PROGRAMMING

## [Functional Programming Concepts](https://medium.com/the-renaissance-developer/concepts-of-functional-programming-in-javascript-6bc84220d2aa#_=_)

- **What is functional programming?**  
"Is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data."

- **What is a pure function and how do we know if something is a pure function?**
Pure function is a function that has the following properties:   
1. -Same Input- Same Output-It returns the same result if given the same arguments (it is also referred as deterministic) 
2. It does not cause any observable side effects.

- **What are the benefits of a pure function?**  
The code’s definitely easier to test. We don’t need to mock anything. 

- **What is immutability?**  
When data is immutable, its state cannot change after it’s created.  
If you want to change an immutable object, you can’t. Instead, you create a new object with the new value.

- **What is Referential transparency?**  
pure functions + immutable data = referential transparency

---

## [Node JS-Modules and require()](https://www.youtube.com/watch?v=xHLd36QoS4k)

- **What is a module?**  
Module is just essentially another javascript file


- **What does the word ‘require’ do?**  
require -> need for a particular purpose.

require method is expected to:  
read the content of a javascript file in a string.  
evaluate that code.  
save the exported function/object in a cache for later use (only read files once)  

- **How do we bring another module into the file the we are working in?**  
use require method as this  
`require('module-Path')` 

- **What do we have to do to make a module available?**  
add in the end of the module file this:  
`module.export = [the part of the module that we want make it availabe outside it]`


