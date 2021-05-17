# Read: 06 - Design web pages with CSS

## Chapter10: Introducing CSS  

The CSS comprises rules, that have 3 parts: a selector, a property, and a value.  
These rules associates with HTML elements  
p{margin:10px} p -> selector | margin -> property | 10px: value
Properties affect how elements are displayed  

### CSS selectors (go to class 3(201-Selector))

*{} -> Selects all elements  
Type selecter (h1, p,..etc) -> elements that matches name  
Class Selector(.note {}) -> Selects all elements with the same class attribute value  
ID Selector -> Selects all elements with the same ID attribute value  
Child Selector (li>a {}) -> selects all a that direct child to li  
Descendant Selector (p a {}) -> selects all a that child to p  (not just a direct child of that p)  
Adjacent Sibling Selector (h1+p {}) -> first p element that after any h1 (next sibling)  
General Sibling Selector (h1~p {}) ->  element that siblings any h1 (not have to be the directly preceding element).
  
### CSS Rules precedence

1.Last rule -> with identical selectors, last one has the most precedence.
2.Specificity -> more specific rule take precedence, example: p#intro is more specific than p
3.Important -> !important after any property value shows that this rule more important than others.

------------------------------

## HTML & CSS, Chapter 11: Color /256-270

### Ways to specify color ->

1. RGB(between 0 and 255) -> rgb(100,100,90)
2. HexCodes -> #ee3e80
3. color names -> red

we can use color pickers; to find any color.

Contrast: a contrast between background and foreground colors; important for readability.
With (Low Contrast) -> text is harder to read. (high Contrast) -> becomes easier to read. (Medium Contrast) -> For long spans of text, we can improve readability by reducing the contrast a little.

Opacity, rgba(alpha value-> between 0.0 and 1.0 ): just like RGB value, but the fourth value is alpha value that indicates opacity; .5 = 5%.

HSL Colors:

1. Hue -> a degree on the color circle from 0 to 360.
2. saturation -> is the amount of gray in a color; 100% full saturation & 0% shade to gray.
3. lightness -> "is the amount of white (lightness) or black (darkness) in a color." -0% lightness is black, 100% lightness is white-

an opacity value for HSL is HSLA.
