# Introduction to React and Components

## Article: Component Based Architecture

- **What is a component?**
A component is a modular, portable, replaceable, and reusable set of well-defined functionality that encapsulates its implementation and exporting it as a higher-level interface.

- **What are the charactistics of a component?**
1. **Reusability**.
2. **Replaceable** -> (components may be freely substituted with other similar components).
3. **Not context specific** -> (Components are designed to operate in different environments and contexts).
4. **Extensible** −> A component can be extended from existing components to provide new behavior.
5. **Encapsulated** −> A component Do not expose details of the internal processes or any internal variables or state.
6. Independent −> Components are designed to have minimal dependencies on other components.

- **What are the advantages of using component based architecture?**
1. **Ease of deployment** −> Easy to replace existing versions to new compatible versions with no impact on the other components or the system as a whole.

2. **Reduced cost** −> The use of third-party components allows you to spread the cost of development and maintenance.

3. **Ease of development** −> Components implement well-known interfaces to provide defined functionality, allowing development without impacting other parts of the system.

4. **Reusable** − Reusable components be used to spread the development and maintenance cost.

5. **Modification of technical complexity** −> A component modifies the complexity through the use of a component container and its services.

6. **Reliability** −> The overall system reliability increases since the reliability of each individual component enhances the reliability of the whole system via reuse.

7. **System maintenance and evolution** −> Easy to change and update the implementation without affecting the rest of the system.

8. **Independent** −> Independent development of components by different group in parallel. 
---
### Notes:
- The primary objective of component-based architecture -> is to ensure component reusability. 
- Some component frameworks: COM/DCOM, JavaBean, EJB, CORBA, .NET, web services, and grid services.
- Advantages of Component-oriented software design over the traditional object-oriented approaches:
1. Reduced time-> by reusing existing components.
2. Increased reliability with the reuse of the existing components.
- Each component has its own interface that specifies required ports and provided ports; each component hides its detailed implementation.
- A component should be extended without the need to make internal code or design modifications to the existing parts of the component.
---
## Artcle: What is Props and How to Use it in React

- **What is props short for?**
is a special keyword in React, stands for Properties 
- **How are props used in React?**
1. Firstly, define an attribute and its value(data)
2. Then pass it to child component(s) by using Props
3. Finally, render the Props Data
- **What is the flow of props?**
A uni-directional flow(one way from parent to child).
---
### Notes:
- Props: A way of passing data from one component to another, used when components need to communicate.
- Props data is read-only, (data coming from the parent should not be changed by child components).
---
## Bookmark/Skim Notes:

- A component takes in parameters called *props*, and returns a hierarchy of views to display via the *render* method.

