# Readings: In memory storage

## [Understanding the JavaScript Call Stack](https://medium.freecodecamp.org/understanding-the-javascript-call-stack-861e41ae61d4)

- **What is a ‘call’?**  
The call stack is primarily used for function invocation (call).

- **How many ‘calls’ can happen at once?**  
 Since the call stack is single, function(s) execution, is done, one at a time, from top to bottom. It means the call stack is synchronous.

- **What does LIFO mean?**  
 Last In, First Out - the last function that gets pushed into the stack is the first to be pop out, when the function returns.

- **Draw an example of a call stack and the functions that would need to be invoked to generate that call stack.**  
```
function firstFunction(){
  console.log("Hello from firstFunction");
}

function secondFunction(){
  firstFunction();
  console.log("The end from secondFunction");
}

secondFunction();
```
- **What causes a Stack Overflow?**  
A stack overflow occurs when there is a recursive function (a function that calls itself) without an exit point.
The browser (hosting environment) has a maximum stack call that it can accomodate before throwing a stack error.

---
## [JavaScript error messages](https://codeburst.io/javascript-error-messages-debugging-d23f84f0ae7c)

- **What is a ‘refrence error’?**  
This Error ocurrs when you try to use a variable that is not yet declared

- **What is a ‘syntax error’?**  
occurs when you have something that cannot be parsed in terms of syntax

- **What is a ‘range error’?**  
occurs when you give an object invalid length.

- **What is a ‘type error’?**  
When the types (number, string and so on) you are trying to use or access are incompatible, like accessing a property in an undefined type of variable.

- **What is a breakpoint?**  
A breakpoint is an intentional stopping or pausing place in a program, put in place for debugging purposes. It is also sometimes simply referred to as a pause

- **What does the word ‘debugger’ do in your code?**  
It achieves the breakpoint
-you can put a debugger statement in your code in the line you want to break.-


<!-- Additional Resources
(JavaScript errors reference on MDN)[https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Errors] -->