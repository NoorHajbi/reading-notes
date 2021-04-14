# Read: 13b - CSS Transforms, Transitions, and Animations
## Article1: What Google Learned From Its Quest to Build the Perfect Team

- From Rozovsky's story and the paper i realized that individual work "No matter of his/her effort" is not enough, a team-based work is more efficient and achieve better results.
-  If a company wants to outstrip its competitors, it needs to influence not only how people work but also how they work together.
- As The researchers eventually concluded that what distinguished the **good** teams from the dysfunctional groups was how teammates treated one another. The right norms, in other words, could raise a group’s collective intelligence, whereas the wrong norms could hobble a team, even if, individually, all the members were exceptionally bright, -it is not required to teams to behave in the same ways-.
- The common thing is that team members understand each other.
---
## Article2: CSS Transforms
### 2D
1. The **transform** property comes in two different settings, two-dimensional(x,y) and three-dimensional(x,y,z).
2. **2D Rotate** -> The rotate value provides the ability to rotate an element from 0 to 360 degrees. Using a positive value will rotate an element clockwise, and using a negative value will rotate the element counterclockwise. *ex: ` transform: rotate(-55deg);`*
3. **2D Scale** -> change the appeared size of an element, The default scale value is 1 (which less than 1 smaller, and greater appears larger) *ex: transform: scale(.75);*.
4. **2D Translate** ->The translate value works a bit like that of relative positioning, Using the translateX value will change the position of an element on the horizontal axis while using the translateY value will change the position of an element on the vertical axis.*ex: `transform: translate(-10px, 25%);` And `transform: translateY(25%);`* 
5. **2D Skew** -> Using the skewX value distorts an element on the horizontal axis while the skewY value distorts an element on the vertical axis. To distort an element on both axes the skew value is used, declaring the x axis value first, followed by a comma, and then the y axis value.
*ex:* 
```
 .box-1 {
  transform: skewX(5deg);
}
.box-2 {
  transform: skewY(-20deg);
}
.box-3 {
  transform: skew(5deg, -20deg);
}
```
- we can combine **skew** and **transform**. *ex: `transform: skew(10deg, 20deg) translateX(20px);`*
- Also we can combine all of them.
### 3D
1. **Perspective** -> In order for three-dimensional transforms to work the elements need a perspective from which to transform. The perspective for each element can be thought of as a vanishing point, similar to that which can be seen in three-dimensional drawings.*ex: ` transform: perspective(200px) rotateX(45deg);`*
2. **3D Scale** -> *ex: `transform: perspective(200px) scaleZ(.25) rotateX(45deg);`*.
3. **3D Translate**-> *ex:`transform: perspective(200px) translateZ(50px);`*. 
4. **3D Skew** -> Skew is the one two-dimensional transform that cannot be transformed on a three-dimensional scale.
---
## Article3: CSS Transitions & Animations
- **Transitions** -> for a transition to take place, an element must have a change in *state,  like using the :hover, :focus, :active, and :target pseudo-classes.*
*Example:*
```
.box {
    background: #2db34a;
    border-radius: 6px
    transition-property: background, border-radius;
    transition-duration: 1s;
    transition-timing-function: linear;
  }
  .box:hover {
    background: #ff7b29;
    border-radius: 50%;
  }

```
- Not all properties may be transitioned.
- **Transition Timing** ->The transition-timing-function property is used to set the speed in which a transition will move. A transition can have multiple speeds within a single duration. has a keyword values like **linear, ease-in, ease-out, and ease-in-out**.
- **ShortHand transition Example:** `transition: background .2s linear, border-radius 1s ease-in 1s;`.
---
- Animations **Keyframes** -> To set multiple points at which an element should undergo a transition.
```
@keyframes slide {
  0% {
    left: 0;
    top: 0;
  }
  50% {
    left: 244px;
    top: 100px;
  }
  100% {
    left: 488px;
    top: 0;
  }
}

```
- Animations behave similarly to transitions. They include a duration, timing function, and delay if desired.
```
.example:hover {
  animation-name: slide;
  animation-duration: 2s;
  animation-timing-function: ease-in-out;
  animation-delay: .5s;
}
```
<!-- Customizing Animations https://learn.shayhowe.com/advanced-html-css/transitions-animations/#customizing-animations-->
---
## Article4: 8 simple CSS3 transitions that will wow your users
1. **Fade in effects** ->using opacity and hover, *Example:*
```
.fade
{
    opacity:0.5;
}
.fade:hover
{
    opacity:1;
}
```
2. **Change color** using color and hover.
3. **Grow & Shrink** using transform and hover.*Example:*
```
.grow:hover
{
        -webkit-transform: scale(1.3);
        -ms-transform: scale(1.3);
        transform: scale(1.3);
}
```
- for grow values more than 1, and less than 1 for shrink.
4. **Rotate elements** using rotate and hover.
5. **Square to circle** using border-radius and hover *Example:*
```
.circle:hover
{
    border-radius:50%;
}
```
6. **3D Shadow** *Example:*
```
.threed:hover
{
        box-shadow:
                1px 1px #53a7ea,
                2px 2px #53a7ea,
                3px 3px #53a7ea;
        -webkit-transform: translateX(-3px);
        transform: translateX(-3px);
}
```
7. **Swing** using @keyframes, animation and animation-iteration and  hover. 
<!--See Swing example: https://www.webdesignerdepot.com/2014/05/8-simple-css3-transitions-that-will-wow-your-users-->
8. **Inset border** *Example*:
```
.border:hover
{
        box-shadow: inset 0 0 0 25px #53a7ea;
}
```



<!-- https://codepen.io/retyui/pen/ByoaXV -->
<!-- https://codepen.io/akshaychauhan/pen/oAfae -->
<!--https://codepen.io/kieranfivestars/pen/MYdQxX-->
<!-- https://codepen.io/dp_lewis/pen/gCfBv -->