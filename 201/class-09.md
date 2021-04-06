# Read: 09 - Forms and Events

## From the Duckett HTML book:

## Chapter 7: Forms (p.144-175)
### Form Controls:
- adding text:
1. Text input (single-line).
2. Password input.
3. Text area (multi-line).
- Making Choices:
1. Radio buttons.
2. Checkboxes.
3. Drop-down boxes.
- Submitting Forms:
1. Submit buttons.`<input type="submit"`
2. Image buttons.`<input type="image" src="">`
- Uploading Files:
1. File upload.

### Form Structure:
1. `<form>` element with action attribute(Value: URL), and method(Value: get/post).
2. `<input>` element, which can be: text/radio//submit/button.
3. Drop Down List Box -> `<select>` element (to create a drop down list box) which includes `<option>` element with value & selected attributes.
4. Multiple select box, `<select>` element that includes size&multiple.
5. File Input Box -> to allow use insert file `<input type="file"`.
6. To group related form controls together use: `<fieldset> element`.
and others.
---
## Chapter 14: Lists, Tables & Forms (pp.330-357)
- `list-style-type` CSS property -> has ordered and unordred list values.
- `list-style-image: url("");`applied with `ul`, to include an image for each li.
- `list-style-position` values are: inside & outside.
- `list-style`-> list shorthand.
- If you have empty cells in your table, use the `empty-cells property` has three values: 1. `show` -> shows the borders of any empty cells. 2. `hide` -> hides the borders of any empty cells. 3.`inherit` -> can inherit nested tables.
- Gaps Between Cells use :`border-spacing(Borders are separeted) or  border-collapse(Borders are collapsed into a Single border)`.
- `cursor` property -> to style mousr cursor.
---
## From the Duckett JS book:
## Chapter 6: Events (pp.243-292)
- Event handling -> how events trigger JS code.
- Event Handling(1. Interactions create events,2, Events trigger,3. Code responds to users). 
### UI Events -> occur when a user interacts with the browser's user interface (ui) rather than the web page:
1. Load -> Web page has finished loading.
2. Unload -> Web page is unloading (usually because a new page was requested).
3. Error -> Browser encounters a JavaScript error, or an asset doesn't exist.
4. Resize -> Browser window has been resized.
5. Scroll -> User has scrolled up or down the page.

### KeyBoard Events -> occur when a user interacts with the keyboar:
1. Keydown -> user first presses a key (repeats while key is depressed)
2. Keyup -> user releases a key.
3. Keypress -> character is being inserted (repeats while key is depressed).

### Mouse Events -> Occur when a user interacts with a mouse, trackpad, or touchscreen
1. Click -> user presses and releases a button over the same element.
2. Dbl click -> user presses and releases a button twice over the same element.
3. Mousedown -> user presses a mouse button while over an element.
4. MouseUp -> user releases a mouse button while over an element.
5. Mousemove -> user moves the mouse (not on a touchscreen).
6. Mouseover -> user moves the mouse over an element (not on a touchscreen).
7. Mouseout -> user moves the mouse off an element (not on a touchscreen).
<!-- See page 247 for more events -->
---
- Events `Fire` / are `Raised` -> (when event occur).
- Events `Trigger a function or script` -> "When the click event fires on the element in this diagram, it could trigger a script that enlarges the selected item. "
- **Binding** is the process of stating which event you are waiting to happen, and which element you are waiting for that event to happen upon. 

### THREE WAYS TO BIND AN EVENT TO AN ELEMENT:
1. HTML EVENT HANDLERS(it is bad to use it, not recommended). *ex: `<input onblur`*
2. TRADITIONAL DOM EVENT HANDLERS. *Syntax-> `element .onevent functionName ;`*
3. DOM LEVEL 2 EVENT LISTENERS.*Syntax-> `element .addEventlistener('event', functionName [, Boolean]) ;`*

### The event object has methods that change: the default behavior of an element and how the element's ancestors respond to the event:

1. "preventDefault() -> tells the user agent that if the event does not get explicitly handled, its default action should not be taken as it normally would be. 
2. stopPropagation() -> prevents further propagation of the current event in the capturing and bubbling phases.
3. Use both -> preventDefault() event continues to propagate as usual, unless one of its event listeners calls stopPropagation() or stopImmediatePropagation(), either of which terminates propagation at once. " [4]
---
- **Event delegation** technique by which you add a single event handler to a parent element in order to avoid having to add event handlers to multiple child elements.
-  **W3C DOM** events are most common used.


