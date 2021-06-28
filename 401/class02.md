# Read: 02 - Arrays, Loops, Imports

## [Java Imports (ignore the parts about NetBeans)](https://perso.ensta-paris.fr/~diam/java/online/notes-java/language/10basics/import.html)

### Packages and Import
- Package = directory.

- The statement order is:
1. Package statement (optional).
2. Imports (optional).
3. Class or interface definitions.

- if import statement finished with **(*)** means '*all classes with that package are available to your program*', or we can specify single class.

### Common imports
```
import java.awt.*;	Common GUI elements.
import java.awt.event.*;	The most common GUI event listeners.
import javax.swing.*;	More common GUI elements. Note "javax".
import java.util.*;	Data structures (Collections), time, Scanner, etc classes.
import java.io.*;	Input-output classes.
import java.text.*;	Some formatting classes.
import java.util.regex.*;	Regular expression classes.
```

-  importing all classes don't make my object file larger, it just tells the compiler where to look, also it is not less efficient .


## [Different types of loops in Java](https://www.baeldung.com/java-loops)

### Java types of loops:

1. for loop (repeat certain operations by evaluating loop counter)
2. Enhanced for-each loop (easier to iterate)
3. While loop (while expression is true, keep loop)
4. Do-While loop (like while, but it execute the statement at least once)