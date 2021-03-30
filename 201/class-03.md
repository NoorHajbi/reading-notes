# Read: 03 - HTML Lists, CSS Boxes, JS Control Flow  
  
## From the Duckett HTML book:  
### Chapter 3: Lists (pp.62-73)  
  
#### List type:  
1. Ordered lists->  where each item in the list is ordered.  `<ol>`  
2. Unordered lists-> where each item in the list begins with a bullet point. `<ul>`  
3. Definition lists-> formatted with term and definition, used to define terminology. `<dl>`: for definition list. `<dt>`: for term. `<dd>`: for definition.   

---
- `<li>`: is for each item in list.
- lists can be nested.
---
### Chapter 13: Boxes (pp.300-329)

- CSS treats each element in HTML document as a box.
- To set box dimensions -> use width and height.
- for limiting width to fit the user's screen -> use: min-width (the minimum size for a screen to display), max-width (maximum size).
- also for limiting height -> min-height, max-height.
- Overflowing content using overflow property;  when content overflows box(larger than box), so this property tells the browser what to do in this case.
- *Over flow has to values: * 
  
| **Overflow values** |       1. hidden        |     	2. scroll                |
| --------------------|------------------------|-------------------------------|
|    **purpose**      |hides any extra content |	adds a scrollbar to the box  |  

---  
- padding -> space around the content itself.
- Border ->  goes around the padding and content.
- Margin -> space outside the border.
---
+ In CSS you can control the border width using -> border-width property
+ border styles that can be added -> dotted, dashed, solid, double, groove, ridge, inset, outset, none, hidden.
+ border-color property -> to specify color.
+ text-align: center; -> for centering content.
+ Display property values-> inline, inline-block(set a width and height on the element.), block (like inline-block but adds line-break after the element).
+ visibility propert values -> hidden, visible.
+ border-image Property -> Specify an image as the border around an element.
+ box-shadow property -> adds shadow around the box.
+ border-radius property - > to control the cornor of box and how much we can make it rounded.
---
## From the Duckett JS book:

### Review from Reading 02 - Chapter 2: “Basic JavaScript Instructions” (pp.70-73)  
  
- Array is a variable that stores a list of values.  
Var class = [1, 2, 3]; -> in this example variable class holds 3 values, each value has an index that starts at 0, so the first index is 0, the second is 1, and so on.  
to change the value of second index -> class[1]= 5;
---
### Chapter 4: “Decisions and Loops” from switch statements on (pp.162-182)
if else statement; checks each condition, and execute first one that returns true.

Switch statement: tests the value of a variable and compares it with multiple cases.

for multiple choices if statement is slower beacuse it checks all even if a match has been found, but with switch when the correct case is found break statement stops rest.

you can ignore using else with if statement.

converting a value from one type to another called Type coercion

When boolean treated as a number -> 0 for false, 1 for true. example: false ==0 (returns true), but false ===0 (returns false).

NaN property "Not-a-Number" indicates that a value is not a legal number.

flasy values treated as false, and not equivalent to anything.

Undefined, NaN, and null -> are falsy values. 

example: NaN == NaN (returns false)

---

#### Three common types of loops: 
1)For -> Syntax:  
for (Initialization; Condition; Update) {  
  // code block to be executed  
}  

- Use: as long the counter does not reache a specified number loop is executed 

2)While -> Syntax:  
while (condition) {  
  // code block to be executed  
}  

- Use->   as the condition returns true, the loop is executed.


3)Do while    -> Syntax  

do {  
  code block to be executed  
}  
while (condition);  

- Use -> loops through a block of code once; then the condition is evaluated.  
  

