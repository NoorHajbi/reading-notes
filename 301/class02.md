# Readings: State and Props

1. **Based off the diagram, what happens first, the ‘render’ or the ‘componentDidMount’?**
Render
2. **What is the very first thing to happen in the lifecycle of React?**
  createing and inserting instance of a component 
3. **Put the following things in the order that they happen: *componentDidMount*, *render*, *constructor*, *componentWillUnmount*, *React Updates***
constructor, render, componentDidMount, React Updates, componentWillUnmount.
4. **What does *componentDidMount* do?**
If you need to load anything using a network request or initialize the DOM, it should go here.
so it used, to connect to the websites API and get output when the components is rendered

---
1. **What types of things can you pass in the props?**
Components and functions
2. **What is the big difference between props and state?**
state is handeled in the component and you can update it inside the component while props are handled outside the component and must be updated outside of the component.

3. **When do we re-render our application?**
when stores something into application.
4. **What are some examples of things that we could store in state?**
Information that updating,like: Counter

Reading
**React lifecycle** https://medium.com/@joshuablankenshipnola/react-component-lifecycle-events-cb77e670a093


Additional Resources
**React Bootstrat Documentation** https://react-bootstrap.github.io/
**Netlify**https://www.netlify.com/

https://www.youtube.com/watch?v=IYvD9oBCuJI


Bookmark/Skim
**React Docs - State and Lifecycle** https://reactjs.org/docs/state-and-lifecycle.html
**React Docs - handling events** https://reactjs.org/docs/handling-events.html
**React Tutorial through ‘Developer Tools’** https://reactjs.org/tutorial/tutorial.html