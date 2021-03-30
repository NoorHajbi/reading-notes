# Read: 04 - HTML Links, CSS Layout, JS Functions  

## From the Duckett HTML book:  
### Chapter 4: Ch.4 Links (pp.74-93)  

-URL(Uniform Resource Locator) -> the web address that is in browser tab when you are in specific web page.
- links allow you to move from one web page to another.
- Links are created using the `<a>` element, and it's attribute that called href.
- `<a>` also links files.
- when another website is linked, the URL called **absolute**.
- when files and folders are linked, the URL called **relative**.
- `<a href="URL OR file">Link text</a>` 
- The top-level folder (root folder) -> contains all the other files and folders for a website, so it considers as a parent for child folders and files, and grandparent for grandChild files and folders.
- the website homepage folder called -> index.html

#### Relative URLs:  

- ../ used to describe parent folder (folder that above the current one) & ../../ for grandparent folder.
- example that describes grandparent folder `<a href="../../index.html">Home</a>` .
- **mailto**  for email links: example `<a href="mailto:noor.hjabi@gmail.com">Noor email</a>`
- `target="_blank` to make linked opened in a new tab.
- To Link to a Specific Part of the Same Page we can identify an ID for that part then use the is like: `<a href="#id">ID</a>`.

---
### Chapter 15: Layout (pp.358-404)

- **block-level element** is any element that starts a new line; example `<p>`
- CSS treats each html element as a block-level box or an inline box.
- **block-level box** that when block-level element is used; Block-level boxes start on a new line.
- **the containing or parent element** An outer block-level box that has a block-level box inside it.
- without the position property;  Browsers display pages in normal flow.
#### The position Property most values are:  
1. **static**(which is a default value for position Property) it is always positioned according to the normal flow of the page.
2. **relative** is positioned relative to its normal position. we can specify top bottom left right values when using it. 
3. **absolute** allows to  place any element exactly where you want
4. **fixed**  like absolutely positioned elements(It is taken out of normal flow); but fixed elements do not affect the position of surrounding elements.

- **Floating Elements** aposition the to the far left or right of a containing box(take it out of the flow).
- **z-index** allows you control position values (relative, fixed, or absolute) which element sits on top of others.
- **Clear** : Clearing the *float* of the next element.
- **Grid Layout** offers a grid-based layout system, with rows and columns.
- multiple CSS files can be included in the same page.
---
## From the Duckett JS book:
### Chapter 3 (first part): Functions, Methods, and Objects (pp.86-99 ONLY)
- **functions and methods** are a series of statements that perform a specific task. 
- functions are reusable.
- to declare a function; function keyword followed by function name is required -> *ex:* function mul(p1, p2) {document.write (p1*p2);}  
- to excute a function you need to do **calling** -> *ex:* mul(1, 2);
- **return** is a keyword used in function when we need to return result.
- A function with no name is called an **anonymous function** -> *ex* mul = function (p1,p2){return p1*p2;};
-  (Immediately Invoked Function Expression) it runs as soon as it is defined.


---
# Article: 6 Reasons for Pair Programming  

### Pair programming roles: the Driver and the Navigator.
- **Driver** who executes everything and writes codes.
- **Navigator** who guides the driver, by thinking about the big picture; like how to covert an algorithm to code.
- Navigator should not be writing any code.
-  **pair program** maybe will take more time to write a code, but it is more efficiency while the code will need less maintenance and more quality.

