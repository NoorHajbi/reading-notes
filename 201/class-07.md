# Read: 07 - HTML Tables; JS Constructor Functions


## Article : Domain Modeling
- **Domain modeling** describes the various entities, their attributes and behaviors, as well as the constraints that govern the problem domain.
-  An entity that stores data in properties and encapsulates behaviors in methods is commonly referred to as an **object-oriented model**.

### Define a constructor and initialize properties
-> To define the same properties between many objects

- The **new** keyword **instantiates** (creates) an object.
- The *constructor* function **initializes** properties inside that object using the *this* variable.
- The object is stored in a variable for later use.
*ex:* `this.name = username;`

Methods:
- **Math.random()** -> to generate random numbers.
- **Math.round** -> eturns the value of a number rounded to the nearest integer.

---
## From the Duckett HTML book:

## Chapter 6: Tables (pp.126-145)
- **Table** represents information in a grid format. 
- `<table>` ->  element used to create a table.
- `<tr>` -> stands for table row.
- `<td>`-> cell in the row(data).
- `<th>` -> like `<td>` but for headings.
- `colspan attribute for <th> & <td> elements` ->  indicates how many columns
that cell should run across.
- `colspan attribute for <tr>` -> hstretch down across more than one row.
- `<thead> <tbody> <tfoot>` -> for table head, body, and foot.
- **Cellpadding attribute** -> to add space inside each cell of the table.
- **Width attribute** -> indicate an element width.
- **bgcolor attribute** -> to indicate background colors of either the entire table or individual table cells.
- **border attribute** -> to indicate the width of the border in pixels.

---
## From the Duckett JS Book:

## Chapter 3: Functions, Methods, and Objects (pp.106-144)
- An **object** is a series of variables and functions.
- Object variable -> Called **property**.
- Object function -> Called **method**.
- To update the value of property use dot notation; *like: `object.PropertyName = PropertyValue;`* if the object does not have that property, it will be added to the object.
- also can be updated using square brackets, *like: `object['PropertyName'] = PropertyValue;`*
- if you want several objects represent the similar things, use constructor.
- A **constructor** is a function that creates an **instance(Object)** of a class.
- **constructor()** method is called automatically when a class is initiated.
- if you do not have a constructor method, JavaScript will add an invisible and empty constructor method.
- "A class cannot have more than one constructor() method. This will throw a **SyntaxError**."[2]
- "In a constructor function this does not have a value. It is a substitute for the new object. The value of this will become the new object when a new object is created."[3]
- You can use the super() method to call the constructor of a parent class.
- You can Add a Method to a Constructor.
- You can use an **array or object** to group a set of related values.
- In JavaScript, data(variables/arrays/objects/) is represented using name/value pairs. 
-  The name in arrays and objectsis -> called **key**.
-  Each key in the object must be unique.
- Array is special type of object.
- **Objects and Arrays** -> are mutable and can be used to store a collection of data.
- Objects can holds array, and vice versa.
- **Three Groups of built in objects:**
1. Browser object model(Model of browser tab) -> (Window(current tab)-> Document(current web page)->History->location(current page URL) ->Navigation-> screen)
2. Document object model (DOM).
3. Global Javascript objects -> starts with capital letter, *eg: String | Number |Boolean | Date | Math | Regex*
- The primitive data types are objects.*{} instead of -> new Object() | "" instead of -> new String(), etc*
