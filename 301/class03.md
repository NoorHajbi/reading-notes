# Readings: Passing Functions as Props

## Article: Lists and Keys

- **What does .map() return?**
Array 
- **If I want to loop through an array and display each value in JSX, how do I do that in React?**
we can embed a loop code in curly braces  
- **Each list item needs a unique** __Key__.
- **What is the purpose of a key?**
Keys help React identify which items in list have changed, are added, or are removed. 

----

## Article: The Spread Operator

- **What is the spread operator?**
The spread operator(…) takes in an iterable (e.g an array) and expands it into individual elements. 

is a useful and quick syntax for adding items to arrays, combining arrays or objects, and spreading an array out into a function’s arguments.
- **List 4 things that the spread operator can do.**
1. spreads the array into separate function’s arguments.
2. adding items to arrays/lists.
3. combining arrays or objects.
4. Adding to state in React

- **Give an example of using the spread operator to combine two arrays.**
`const ourArray = [...myArray,...yourArray]`
- **Give an example of using the spread operator to add a new item to an array.**
`const fewMoreFruit = ['🍉', '🍍', ...fewFruit]`
- **Give an example of using the spread operator to combine two objects into one.**
`const objectFour = {...objectOne, ...objectTwo, laugh: () => {console.log("😂".repeat(5))}}`
---

## Video : How to Pass Functions Between Components

- **In the video, what is the first step that the developer does to pass functions between components?**
create a parameter and we need it to be passed  in object

- **In your own words, what does the increment function do?**
each loop, one object will be passed inside a loop, so it would check the name as this expression (if p.name=name) when it matches, the count will be incremented, and finally the state will be updated.

- **How can you pass a method from a parent component into a child component?**
1. in a render function(that get data from a child component) in the parent component. 
we can pass a method inside a child object which inside that function.

- **How does the child component invoke a method that was passed to it from a parent component?**
pass the method as a prop in child component.
