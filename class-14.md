# Transforms:

## Perspective

Transform Syntax : (vanishing point)
he **perspective** of an element can be set in two different ways. One way includes **using the perspective value within the transform property on individual elements(transform single element)**, while the other includes**using the perspective property on the parent element residing over child elements being transformed.(transform a group of elements )**

```
div {

          transform: scale(1.5);
}
```
It is common for multiple transforms to be used at once, rotating and scaling the size of an element at the same time.


**he transform property comes in two different settings** :

**1-2D Transforms**

 work on the x and y axes, known as horizontal and vertical axes. 

 values : 

 The `rotate` value provides the ability to rotate an element from 0 to 360 degrees.
 ```
 .box-1 {
  transform: rotate(20deg);
}
```
  `scale ` change the appeared size of an element
   The default scale value is **1**, therefore any value between **.99** *and **.01** makes an element appear **smaller** while any value greater than or equal to **1.01** makes an element appear **larger**.

   ```
   .box-1 {
  transform: scale(.75);
}
```
to scale x and y values use :
```
.box-3 {
  transform: scale(.5, 1.15);
}
```


`translate ` : like relative positioning (does not affect the flow )
pushing and pulling an element in different directions 


`2D Skew`  distort elements on the horizontal axis, vertical axis, or both .
```
box-1 {
  transform: skewX(5deg);
}
```
`Transform Origin` 
default transform origin is the dead center of an element, both 50% horizontally and 50% vertically. 


**2- 3D Transforms**
change elements on the x ,y and z axis.


`3D Rotate` 

```
.box-3 {
  transform: perspective(200px) rotateZ(45deg);
}
```



`3D Scale`

`3D Translate` A negative value here will push an element further away on the z axis, resulting in a smaller element.



`3D Skew`
Skew is the one two-dimensional transform that cannot be transformed on a three-dimensional scale so Elements may be skewed on the x and y axis, then transformed three-dimensionally as wished.

`transform style` To allow nested elements to transform in their own three-dimensional plane ,needs to be placed on the parent element, above any nested transforms. 

## Backface Visibility
set `backface-visibility `property to hidden, and you will hide the element whenever it is facing away from the screen.


# Animations:
llow the appearance and behavior of an element to be altered in multiple keyframes.


## Transitions  :
for a transition to take place, an element must have a change in state, and different styles must be identified for each state.

### There are four transition related properties : 

1-Transitional Property :
The `transition-property` property determines exactly what properties will be altered in conjunction with the other transitional properties.

** not all properties may be transitioned, only properties that have an identifiable halfway point.**


2-Transition Duration
`transition-duration` The duration in which a transition takes place

3-Transition Timing
`transition-timing-function` property is used to set the speed in which a transition will move. 

keyword values for the transition-timing-function property include `linear`, `ease-in`, `ease-out`, and` ease-in-out`.

4-Transition Delay
`transition-delay`  The delay sets a time value, seconds or milliseconds, that determines how long a transition should be stalled before executing.


**Shorthand Transitions**
Using the `transition` value alone, you can set every transition value in the order of `transition-property`, `transition-duration`, `transition-timing-function`, and  `transition-delay`

```
.box {
  background: #2db34a;
  border-radius: 6px;
  transition: background .2s linear, border-radius 1s ease-in 1s;
}
```


# Animations : 


1-Animations Keyframes :(`@keyframes`) points at which an element should undergo a transition

2-Animation Name
sing the `animation-name` property alone isn’t enough  need to declare an `animation-duration` property and value so that the browser knows how long an animation should take to complete.


### Animations also provide the ability to further customize an element’s behavior


1- To have an animation repeat itself numerous times the `animation-iteration-count` property

2-Animation Direction
declare the direction an animation completes using the `animation-direction`
it can have these values :  `normal`, `reverse`, `alternate`, and `alternate-reverse`

3-Animation Play State 
The `animation-play-state` property allows an animation to be played or paused using the `running` and ` paused` keyword values

4-Animation Fill Mode :
` animation-fill-mode` property identifies how an element should be styled either before, after, or before and after an animation is run
values are :` none`, `forwards`, `backwards`, and `both`.

## Shorthand Animations:

```
.stage:hover .ball {
  animation: slide 2s ease-in-out .5s infinite alternate;
}
```


# css transtions examples :

1. Fade in : by changing the opacity
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

2. Change color

3. Grow & Shrink ( use CSS3’s transform)

4. Rotate elements(using transform)
```
.rotate:hover
{
        -webkit-transform: rotateZ(-30deg);
        -ms-transform: rotateZ(-30deg);
        transform: rotateZ(-30deg);
}
```
5. Square to circle (using boreder radius)
```
.circle:hover
{
        border-radius:50%;
}
```
6. 3D shadow (use box shadow)
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
7. Swing (animation)

8. Inset border

```
.border:hover
{
        box-shadow: inset 0 0 0 25px #53a7ea;
}
```


