# CSS Animation
An animation lets an element gradually change from one style to another.

You will learn about the following properties:
- @keyframes
- animation-name
- animation-duration
- animation-delay
- animation-iteration-count
- animation-direction
- animation-timing-function
- animation-fill-mode
- animation

## Browser Specific Prefixes
Some older browsers need specific prefixes (-webkit-) to understand the animation properties:

Example
```css
div {
  width: 100px;
  height: 100px;
  background-color: red;
  -webkit-animation-name: example; /* Safari 4.0 - 8.0 */
  -webkit-animation-duration: 4s; /* Safari 4.0 - 8.0 */
  animation-name: example;
  animation-duration: 4s;
}

/* Safari 4.0 - 8.0 */
@-webkit-keyframes example {
  from {background-color: red;}
  to {background-color: yellow;}
}

/* Standard syntax */
@keyframes example {
  from {background-color: red;}
  to {background-color: yellow;}
}
```


## The @keyframes Rule
When you specify CSS styles inside the @keyframes rule, the animation will gradually change from the current style to the new style at certain times.

Example
```css
/* The animation code */
@keyframes example {
  from {background-color: red;}
  to {background-color: yellow;}
}

/* The element to apply the animation to */
div {
  width: 100px;
  height: 100px;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
}
```

**Note**: The animation-duration property defines how long time an animation should take to complete. If the animation-duration property is not specified, no animation will occur, because the default value is 0s (0 seconds). 

In the example above we have specified when the style will change by using the keywords "from" and "to" (which represents 0% (start) and 100% (complete)).

It is also possible to use percent. By using percent, you can add as many style changes as you like.

The following example will change the background-color of the  `<div>` element when the animation is 25% complete, 50% complete, and again when the animation is 100% complete:

Example
```css
/* The animation code */
@keyframes example {
  0%   {background-color: red;}
  25%  {background-color: yellow;}
  50%  {background-color: blue;}
  100% {background-color: green;}
}

/* The element to apply the animation to */
div {
  width: 100px;
  height: 100px;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
}
```

The following example will change both the background-color and the position of the `<div>` element when the animation is 25% complete, 50% complete, and again when the animation is 100% complete:

Example
```css
/* The animation code */
@keyframes example {
  0%   {background-color:red; left:0px; top:0px;}
  25%  {background-color:yellow; left:200px; top:0px;}
  50%  {background-color:blue; left:200px; top:200px;}
  75%  {background-color:green; left:0px; top:200px;}
  100% {background-color:red; left:0px; top:0px;}
}

/* The element to apply the animation to */
div {
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
}
```

## Delay an Animation
The animation-delay property specifies a delay for the start of an animation.

The following example has a 2 seconds delay before starting the animation:

Example
```css
div {
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
  animation-delay: 2s;
}
```

Negative values are also allowed. If using negative values, the animation will start as if it had already been playing for N seconds.

In the following example, the animation will start as if it had already been playing for 2 seconds:

Example
```css
div {
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
  animation-delay: -2s;
}
```

## Set How Many Times an Animation Should Run
The animation-iteration-count property specifies the number of times an animation should run.

The following example will run the animation 3 times before it stops:

Example
```css
div {
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
  animation-iteration-count: 3;
}
```

The following example uses the value "infinite" to make the animation continue for ever:

Example
```css
div {
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
  animation-iteration-count: infinite;
}
```


## Run Animation in Reverse Direction or Alternate Cycles
The animation-direction property specifies whether an animation should be played forwards, backwards or in alternate cycles.

The animation-direction property can have the following values:

**normal** - The animation is played as normal (forwards). This is default
**reverse** - The animation is played in reverse direction (backwards)
**alternate** - The animation is played forwards first, then backwards
**alternate-reverse** - The animation is played backwards first, then forwards
The following example will run the animation in reverse direction (backwards):

Example
```css
div {
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
  animation-direction: reverse;
}
```


## Specify the Speed Curve of the Animation
The animation-timing-function property specifies the speed curve of the animation.

The animation-timing-function property can have the following values:

**ease** - Specifies an animation with a slow start, then fast, then end slowly (this is default)
**linear** - Specifies an animation with the same speed from start to end
**ease-in** - Specifies an animation with a slow start
**ease-out** - Specifies an animation with a slow end
**ease-in-out** - Specifies an animation with a slow start and end
**cubic-bezier(n,n,n,n)** - Lets you define your own values in a cubic-bezier function
The following example shows the some of the different speed curves that can be used:

Example
```css
#div1 {animation-timing-function: linear;}
#div2 {animation-timing-function: ease;}
#div3 {animation-timing-function: ease-in;}
#div4 {animation-timing-function: ease-out;}
#div5 {animation-timing-function: ease-in-out;}
```


## Specify the fill-mode For an Animation
CSS animations do not affect an element before the first keyframe is played or after the last keyframe is played. The animation-fill-mode property can override this behavior.

The animation-fill-mode property specifies a style for the target element when the animation is not playing (before it starts, after it ends, or both).

The animation-fill-mode property can have the following values:

**non**e - Default value. Animation will not apply any styles to the element before or after it is executing
**forwards** - The element will retain the style values that is set by the last keyframe (depends on animation-direction and animation-iteration-count)
**backwards** - The element will get the style values that is set by the first keyframe (depends on animation-direction), and retain this during the animation-delay period
**both** - The animation will follow the rules for both forwards and backwards, extending the animation properties in both directions
The following example lets the <div> element retain the style values from the last keyframe when the animation ends:

Example
```css
div {
  width: 100px;
  height: 100px;
  background: red;
  position: relative;
  animation-name: example;
  animation-duration: 3s;
  animation-fill-mode: forwards;
}
```
The following example lets the <div> element get the style values set by the first keyframe before the animation starts (during the animation-delay period):

Example
```css
div {
  width: 100px;
  height: 100px;
  background: red;
  position: relative;
  animation-name: example;
  animation-duration: 3s;
  animation-delay: 2s;
  animation-fill-mode: backwards;
}
```
The following example lets the <div> element get the style values set by the first keyframe before the animation starts, and retain the style values from the last keyframe when the animation ends:

Example
```css
div {
  width: 100px;
  height: 100px;
  background: red;
  position: relative;
  animation-name: example;
  animation-duration: 3s;
  animation-delay: 2s;
  animation-fill-mode: both;
}
```


## Animation Shorthand Property
The example below uses six of the animation properties:

Example
```css
div {
  animation-name: example;
  animation-duration: 5s;
  animation-timing-function: linear;
  animation-delay: 2s;
  animation-iteration-count: infinite;
  animation-direction: alternate;
}
```
The same animation effect as above can be achieved by using the shorthand animation property:

Example
```css
div {
  animation: example 5s linear 2s infinite alternate;
}
```

## Other animation properties.
**animation-play-state** - Specifies whether the animation is running or paused.

Pause an animation:
```css
div {
  animation-play-state: paused;
}
```

CSS Syntax
```css
animation-play-state: paused|running|initial|inherit;
```