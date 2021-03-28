# Read: 02 - HTML Text, CSS Introduction, and Basic JavaScript Instructions  

## From the Duckett HTML book:  

### 1.Chapter 2: Text (pp.40-61)  
- Tags also called markup.

- Structural markup: elements that describe both headings and paragraphs.
`<p> <h1> ..<h6> <sup> <sub> <b> <i> <br/> <hr/> -> horizontal rule between sections. `
-White space collapsing -> blank spaces, newlines, or tabs. `<p> Hello    all </p>`.  

- Semantic markup:  provides extra information, used according to their intended purpose.  ->
`<strong>, <em>, <blockquote>, <q>, <abbr>, <cite>, <dfn>, <address>, <ins> ->(inserted) underlined, <del> -> line through it (show deleted text), <s> output like <ins> but for :  sth that no longer accurate or relevant (not for deleted).`.
`<dfn>` -> define new terminology.
--
### 2.Chapter 10: Ch.10 Introducing CSS (pp.226-245) //rep

- The CSS comprises rules, that have 3 parts: a selector, a property, and a value.  

- CSS selectors:
1. *{} -> Selects all elements  
2. Type selecter (h1, p,..etc) -> elements that matches name  
3. Class Selector(.note {}) -> Selects all elements with the same class attribute value  
4. ID Selector -> Selects all elements with the same ID attribute value  
5. Child Selector (li>a {}) -> selects all a that direct child to li  
6. Descendant Selector (p a {}) -> selects all a that child to p  (not just a direct child of that p)  
7. Adjacent Sibling Selector (h1+p {}) -> first p element that after any h1 (next sibling)  
8. General Sibling Selector (h1~p {}) ->  element that siblings any h1 (not have to be the directly preceding element)
  
- CSS Rules precedence:
1. Last rule -> with identical selectors, last one has the most precedence.
2. Specificity -> more specific rule take precedence, example: p#intro is more specific than p
3. Important -> !important after any property value shows that this rule more important than others.

--
## From the Duckett JS book:  

### Chapter 2: Basic JavaScript Instructions (pp.53-84)  

- JAVASCRIPT IS CASE SENSITIVE
- Script: is a series of instructions that a computer can follow. 
- `//` OR `/* */` for comments.
- DATA TYPES : Number, String, and boolean.
- A number of variables can be declared or assigned or both in the same statement.
- Variable name must begin with letter, dollar sign ($),or an underscore (_).
- Array is a variable that stores a list of values.
-rep-
- Expressions have two types:
 1. expressions that assign a value to a variable; Like name = 'Noor'.
 2. expressions that use 2 or more variables in order to return a value; A= 2+3.  

- Operations:
 1. Assignment operators -> name = 'Noor'
 2. Arithmetic Operators -> uses operators like + - / *%; A= 2+3 
-> A= 5.
 3. Comparison operators -> Compare two or more Values, then return True/False; A= 7>2 
-> A= True.
 4. Logical operators ->  connect two or more expressions, then return True/False.
 5. String operators -> Combine Two or more strings; Major = 'Web' + ' Developer' 
-> Major ='Web Developer'.  

### Chapter 4: Decisions and Loops- only up to the section on switch statements (pp.145-162)  
- Flow charts is steps that help to determine what line of codes should run next.
- Diamond shape is decision point.
- There are two components to a decision:
1. An expression that returns a value.
2. A conditional statement.

- Comparison operators:  
1. (Is equal to ==) -> compares to values.
2. (Strict equal to ===) -> compares to values with data type.
3. (Is not equal to != )
4. (Strict not equal to !== )
5. Other Comparison operators> < >= <=

- Logical Operators: evaluated from left to right. (&& || !)

- If statement is conditional expressions that executed when proved to be true.
- If else -> first true condition is executed, when the condition is false see other(else).
- Switch statement -> tests the value of a variable and compares it with multiple cases.
-------------
# Link : How to Write a Git Commit Message?

- a well-crafted Git commit message is the best way to communicate context about a change to fellow developers.
- `git log` Shows the log of previous commits.
- " In order to create a useful revision history, teams should first agree on a commit message convention"
