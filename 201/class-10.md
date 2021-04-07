# Read: 10 - JS Debugging

## From the Duckett JS book:
## JavaScript book, Ch. 10, Error Handling & Debugging

- the javascript interpreter processes one line of code at a time. So, When a statement needs data from another functionm it **stacks(or piles)** the new function on top of the current task. 
- Each time a new item is added to the stack, it creates a new execution context.
---
### Execution context & Hoisting
- Each time a script enters a new **execution context**, there are two phases
of activity:
1. Prepare -> when creates The new scope/Variables, functions, and arguments/ or determines The value of the this keyword.  
2. Exexcute -> when assign values to variables/Reference functions and run their code/Execute statements.

- For **hoisting**:
• Call functions before they have been declared/Assign a value to a variable that has not yet been
declared .

- Functions in JavaScript are said to have **lexical scope** -> the scope is the current execution context's variables object, plus the variables object for each parent execution context.

- If a JavaScript statement generates an error, then it throws an exception. At that point, the interpreter stops and looks for **exception-handling** code.

- Error objects can help you find where your mistakes are and browsers have tools to help you read them. 

- JavaScript has 7 different types of errors:
1. Syntax Error. 
2. ReferenceError -> When the variable is not declared or is out of scope.  
3. EvalError -> Incorrect use of eval() function.
4. URI Error -> Incorrect use of URI functions.
5. Type Error -> Value is unexpected data type.
6. RangeError -> Number outside of range.
7. Error(The generic Error object) ->Is the template (or prototype) from which all other error objects are created. 
-  NaN (Not An Error)-> Indicates that a value is not a legal number,(JavaScript considers the type of NaN to be number).
---
### How to deal with errors ?
1. Debug the script to fix errors -> track down the source of the error and fix it.
2. Handle errors **gracefully**-> using try, catch, throw, and finally statements(gives user helpful feedbacks).
---
- understand execution contexts and stacks, helps you to find the error in your code. 
- **Debugging (involves process of deduction)**: helps you eliminating potential causes of an error. 
- We can use console to look at errors.

