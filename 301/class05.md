# Readings: Putting it all together

## Article: React Docs - thinking in React
- **How would you break a mock into a component heirarchy?**  
1. (Designer Work) -> Draw boxes around every component (and subcomponent) in the mock and give them all names.
2. To know what should be its own component,Use the same techniques for deciding if you should create a new function or object. One such technique is `the single responsibility principle`.
3. Now that we’ve identified the components in our mock, So to arrange them into a hierarchy -> Components that appear within another component in the mock should appear as a child in the hierarchy.

- **What is the single responsibility principle and how does it apply to components?**  
A component should ideally only do one thing. If it ends up growing, it should be decomposed into smaller subcomponents

- **What does it mean to build a ‘static’ version of your application?**  
To build a version that takes your data model and renders the UI but has no interactivity.

- **Once you have a static application, what do you need to add?**  
build components that reuse other components and pass data using props. 
`Don’t use state at all to build this static version.`

- **What are the three questions you can ask to determine if something is state?**  
1. *Is it passed in from a parent via props?* If so, it probably isn’t state.
2. *Does it remain unchanged over time?* If so, it probably isn’t state.
3. *Can you compute it based on any other state or props in your component?* If so, it isn’t state.  

- **How can you identify where state needs to live?**  
1. *Identify every component that renders something based on that state.*
2. *Find a common owner component `(a single component above all the components that need the state in the hierarchy)`.*
3. *Either the common owner or another component higher up in the hierarchy should own the state.*
- *If you can’t find a component where it makes sense to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common owner component.*
---

