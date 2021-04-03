# Read: 06 - JS Object Literals; The DOM

## Article: Understanding The Problem Domain Is The Hardest Part Of Programming.

### "What is the hardest thing about writing code?
1. Learning a new technology.
2. Naming things.
3. Testing your code.
4. Debugging.
5. Fixing bugs.
6. Making software maintainable, and so on." [1] 
-This part is exactly quoted from the article-

### Before coding you should understand problem domains, which makes writing code easier.

--- 
## From the Duckett JS book:
## Chapter 3: Object Literals (pp.100-105)
- Object contains set of variables and functions.
- Property: a variable that part of object.
- & functions known as mehtods.
- Broperties and methods have a key and a value.
- Key -> is name & object cannot have two keys with the same name.
- Value can be string, number, Boolean, array, or even another object. 
- Dot notation used to access properties and methods of an object. (*ex:* hotel.name | hotel is obejct| name is property or method name)

## Chapter 5: Document Object Model (pp.183-242)
**The Document Object Model (DOM)** set of rules specifies how browsers creates a model  of an HTML page and how JavaScript can access and update the contents of a web page.
- The DOM is called an object model -> because the model (that is called **the DOM tree**) is made of objects.
- **DOM tree nodes**
1. The document node -> Added at the top of the tree and represents the entire page.
2. Element nodes -> Every HTML element -> in element node you can access and update the content using properties such as textContent and innerHTML or using DOM manipulation techniques.
3. Attribute node -> Every HTML attribute.
4. Text node -> The text in the HTML elements.
- **Accessing and updating the DOM tree involves two steps:**
1. Locate the node that represent the element.
+ select an individual element node -> getElementByld () | querySelector ().
+ select multiple elements (nodelists) -> getElementsByClassName() | getElementsByTagName() | querySelectorAll()
+ traversing between element nodes select parentNode | previousSibling | nextSibling| firstChild / lastChild.

2. Use its text content, child elements, and attributes. 
+ **The nodeName Property** -> is readonly & specifies the name of a node.
+ **The nodeValue Property** -> specifies the value of a node.
+ **The nodeType property** -> read-only & specifies the type of node.
+ **DOM querying** -> methods that return live node lists.
+ DOM queries may return one element, or they may return a Nodelist, which is a collection of nodes.
+ **getElementByid()** -> allows you to select a single element node by specifying the value of its id attribute.
+  **NodeList** is returned by the getElementsByTagName() method and the childNodes property.
+ Nodes in the node list are accessed with index numbers starting from 0.
+ DOM query return Node list -> to return more than one node








