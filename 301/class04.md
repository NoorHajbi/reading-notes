# React and Forms

## Article:  Docs - Forms

1. **What is a ‘Controlled Component’?**
 An input form element whose value is controlled by React 

2. **Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.**
We update the state with their responses as soon as they enter them?,In React, mutable state is typically kept in the state property of components, and only updated with setState(),so, React component controls what happens in that form on subsequent user input. 

3. **How do we target what the user is entering if we have an event handler on an input field?**
 'When you need to handle multiple controlled input elements, you can add a name attribute to each element and let the handler function choose what to do based on the value of event.target.name.'


----

## Article: The Conditional (Ternary) Operator 

1. **Why would we use a ternary operator?**
to write a shorter code than the normal if statement
2. **Rewrite the following statement using a ternary statement**
`if(x===y){ console.log(true);} else {console.log(false); }`

 x===y ? console.log(true) : console.log(false);


<!-- Bookmark/Skim
React Bootstrap - Forms
React Docs - conditional rendering -->