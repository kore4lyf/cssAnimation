# CSS Animation 101 - by Donovan Hutchinson

## Todo
- [Save Button Wiggle](http://codepen.io/donovanh/pen/KwEQdQs)
- [Animating List Items](https://cssanimation.rocks/list-items/)
- [Portal animation](http://hop.ie/portal/)
- [Animated transition from A to B](http://codepen.io/donovanh/pen/RNdxqw)
-  [Animated button](http://codepen.io/donovanh/pen/MYQdZd)
-  [More transitions](http://codepen.io/suez/pen/XJGOyL)
-  [Mac Plus created using CSS](http://codepen.io/donovanh/full/HGqjp/)
-  [Button hover effect](http://codepen.io/donovanh/pen/MYQdZd)
-  [Shiny Effect](https://cssanimation.rocks/pseudo-elements/)
-  [Fancy Button](http://codepen.io/donovanh/pen/YPMGpJ)
-  [Cat Hover card](http://codepen.io/donovanh/pen/LEvjJg)
-  [Change Background](http://codepen.io/donovanh/pen/WbqNwd?editors=110)
- [Traffic Light](http://codepen.io/donovanh/pen/ogRRdR?editors=010)


## Chapter 1 - Welcome
### Hello, I’m Donovan
### Book structure
### Help and support
### Need to brush up on your CSS?
### Homework



## Chapter 2 - Why animate?
- “Animation is about creating the illusion of life.” Brad Bird

### More than words alone
- Animation can convey information efficiently and grab attention (Communication).
- Movement in our designs gives us a more powerful way to communicate.
- ubtle and appropriate animation can add appeal to our designs and credibility to our work.
- We’re very good at spotting movement. This is something we have evolved to do. Adding a little animation here and there can introduce some of that “illusion of life” in a very subtle way.

### What is animation on the web?
- We can use animation to tell a story. However,
telling stories through our content doesn’t always need to be so literal. We can add subtle movement, such as showing data changes in a chart. In this way, data can itself tell a story with animation helping.

### With great power comes great responsibility
- It can be easy to do too much with animation. Having too many things moving around on the page at once is distracting.
- Try to do less animation when possible.
- This might mean only moving a small item on your page.
- If you want to create more of a “wow” effect with larger animations, you can do so. Just stop when your viewers need to focus on the content. This might mean setting animations to play once rather than infinitely, or stopping animations when people begin to scroll a page.


### Inspiration
- Animation has a long and rich history. I recently wrote a post on Principles of Animation for the Web. The principles draw from Disney’s 1981 book The Illusion of Life: Disney Animation.
- For loads of great examples, take some time to browse Hover States. This site features all sorts of interesting examples of animation from the web. Dribbble.com is helpful also.

### Summary
- Animation is kind of a big deal
- Used right, it can be a useful and powerful tool in our designs
- Use it to grab attention or convey information
- Don’t overdo it
- If you want to stand out, animation can really help

### Homework
Think about your own work and how animation might help.
Try not to go crazy and animate all the things. Look for ways subtle animation might better help your visitors understand the content. Is there a call-to-action on your page people are missing? Is there a sudden change in your page that’s happening too suddenly, and could benefit from a smoother transition?
Lastly, take a look at sites like **Hover States** and **Little Big Details** and **Dribbble**. These sorts of sites help if you’re ever stuck for ideas.



## Chapter 3 - Creative environments
### In the browse
### Local development
### In summary
### Homework



## Chapter 4 - Transitions
### Transitions
- One way CSS lets us control animation in the browser with the transition property. In browser terms, a transition is an animation from one state to another.
- When we use a transition on an element we tell the browser that we want it to interpolate, or automatically calculate, the change between states.

### Transition properties
### In summary
- A transition is the change from one state to another. For example, when hovering
over an element, its style might change. Transitions allow the change to become
a smooth animation.
### Homework 



## Chapter 5 - Animations
### Animation in the browser 
- While transitions are all about smoothing the change from state A to state B, animations are a way to describe multiple steps.
- Animations are useful for more complex movement in the browser. In the above example, there are 3 states (A, B and C). A transition would only go from A to C while an animation allows us to specify what step B looks like and make sure the animation follows all three steps.
- Animations also behave a little differently. They can begin automatically. While
a transition might require adding a class or a change of state such as hovering,
animations can start when the page loads



### Examples
### Transitions vs Animations
- Transitions are when the browser animates from one state to another (A to B).
They’re usually triggered by an action such hovering over an element, or adding or removing a class using JavaScript.
Animations are more involved, and let you create sequences of animations with
as many key
### Homework



## Chapter 6 - Transitions in action
### Transitions
Transitions take place in the browser when an element changes from one state to another. The browser draws the frames between each state automatically to create movement.

### Example: Button transition
We can write a transition in CSS like this:
```css
transition: background 0.5s linear;
```

The above property might cause a button’s background to change when hovered
over:
```css
button {
background: white;
transition: background 0.5s linear;
}
button:hover {
background: green;
}
```

The important thing to look for is the any property beginning transition-.
I’ve written them out long-hand for demonstration like so:
```css
transition-property: all;
transition-duration: 0.4s;
transition-timing-function: ease-out;
```

For a fun effect, try changing the transition-timing-function value from
ease-out to:
```css
transition-timing-function: cubic-bezier(.59,-0.26,.33,1.42)
```

### Prefixes and browser compatibility
When I’ve given code examples, I’ve not included vendor prefixes. This is to make the code easier to read, but if you’re using the code in production they are needed.
I like to use Autoprefixer (this is an option on Codepen: press the settings “cog” icon in the CSS section), and can be run with build tools such as Grunt or Gulp.
Alternately you can manually write them out like this:
```css
-webkit-transition: ...;
-moz-transition: ...;
transition: ...;
```
### Homework



## Chapter 7 - Transitions properties
### Shorthand vs Longhand
When writing CSS, we can often summarise multiple properties into one in a shorthand property. For example, padding written as shorthand might look like
this:
```css
padding: 10px 20px 15px 25px;
```
This would be the equivalent of:
```css
padding-top: 10px;
padding-right: 20px;
padding-bottom: 15px;
padding-left: 25px;
```
In the same way, we can write a transition as shorthand too:
```css
transition: all 0.5s 1s linear;
```
In this case, the shorthand corresponds to:
```css
transition: [property] [duration] [delay] [timing-function];
```
Each of these properties can be written individually:
```css
transition-property: all;
transition-duration: 0.5s;
transition-delay: 1s;
transition-timing-function: linear;
```


### Things transitions don’t work on
While you can use transitions on positioning, size, colour, border, background-position and many others, there are some that cannot be transitioned. The font-family cannot be transitioned, as this would mean trying to generate frames between two very different font images.
Background images created with CSS, such as generated gradients, cannot have their properties animated. This would mean the browser recreating the background image with each frame of animation and so is not supported.
However you can animate things like opacity and background position. By moving background images around or hiding them you can create interesting effects.


### Homework



## Chapter 8 - Timing functions
The timing function is a description of the rate at which the speed of the transition changes. Animations look lifeless when they occur at a fixed, linear pace.

### Linear
A linear transition moves at a steady rate from beginning to end. Since there’s no curve in the transition, it never accelerates or decelerates. This can be useful if making animations that need a steady movement, like the scenery moving past the background of a train window or a steadily rotating moon.


### Ease-in
The ease-in timing function begins slowly and accelerates toward the end of the transition. It would be similar to a ball beginning to roll down a hill, finishing
at the fastest speed at the bottom.


### Ease-out
Ease-out is the opposite of ease-in. It starts fast and slows down toward the end of the transition. Useful for when something needs to appear as if it was rushing from off-screen and slowing down to stop.


### Ease-in-out
Ease-in-out is a combination of both the ease-in and ease-out functions. It begins slowly, accelerates through the middle part of the transition, then slows toward the end. It could illustrate a car starting from a standstill, accelerating, then slowing down before stopping. If making a loading animation, something like this can look pretty good.


### Cubic-bezier
All the timing functions we’ve seen so far are examples of cubic bezier curve.
This is a curve that describes the “shape” of the timing function.
In this way, specifying a cubic-bezier timing function is like creating a timing function of our own.
They consist of 4 values, representing two co-ordinates. A cubic-bezier can look like this:
transition-timing-function: cubic-bezier(1,-0.49,.13,1.09);
The two co-ordinates here are (1, -0.49) and (.13, 1.09). On a graph, they look like this:
Rather than create these by hand, I use cubic-bezier.com. A great way to create some interesting effects.



### Steps
Where most of the timing functions involve curves, the steps function divides the transition into a set of steps and jumps between each.
The transition divides the duration into 4 discrete jumps (pictured above).

This is useful for sprite animation. For example, a loading spinner or animated video game character. By setting the background position at the beginning of a series of frames, the steps timing function can then be used to jump through each frame and create the appearance of movement.
To see a good example of this in action, check out the Twitter fave button animation.
You can also specify whether the transition holds the first frame for the fragment of the duration or whether it holds the final frame. The default is end, as this assumes that the first frame in the sprite is already showing before the animation begins.
We can specify which applies when setting the steps:
```css
transition: all 2s steps(10, start);
transition: all 2s steps(10, end);
```


### More examples
### Homework



## Chapter 9 - Multiple transitions
Next we’ll see what happens when we apply a single transition to an element with multiple changes, and how to use multiple transitions together to subtly improve our animation.

### Example 1: Fancy button
### Example 2: Background reveal
### Multiple transitions on a single element
We can achieve this by combining multiple transitions into a single declaration.
Multiple transitions are separated by commas.
For example:
```css
transition: background 1s ease-out, border 0.5s linear;
```


### Homework



## Chapter 10 - Transitions and JavaScript
 we’ve been using the transition property in CSS to animate between
two states, a non-hover and a hover (or focus) state.
These transitions have required hovering over the element. This isn’t the only way
we can trigger animations, so today we’ll cover two ways we can use JavaScript
to achieve the same result


### Add or remove classes
Since the power of transitions is to animate between two states, we can create those states as separate classes. Then we add or remove these classes using JavaScript (e.g. hidding an element when a button is clicked).


### Controlling transitions with JavaScript
We can go further than adding or removing classes. Using JavaScript we can set
the CSS properties directly like so:
element.style.transition = 'opacity 1s ease-out';
In this case, “element” is an element we’ve selected. For example, if an element
has the ID “js-show”, you could apply a transition to it using getElementById:
```css
document.getElementById('js-show').style.transition = 'opacity 1s ease-out';
```
When we do this, we must remember to include vendor prefixes too. The above
would need to be written:
```css
document.getElementById('js-show').style.webkitTransition = 'opacity 1s ease-out';
document.getElementById('js-show').style.transition = 'opacity 1s ease-out';
```
Here the webkitTransition applies to any browsers that would otherwise use
the -webkit- prefix in CSS.


### Let’s recap
### Homework



## Chapter 11 -  Animations in action
### A symbiotic relationship
The animation property is applied to an element just like a transition. It also needs a second part, called keyframes.
```css
.element {
animation: ...
}
@keyframes animation-name {
/* Keyframes go here */
}
```

One benefit of having the keyframes defined separately is that it allows us to create animations that can be reused multiple times.


### The animation property
. An animation
could be written as the following shorthand:
```css
animation: change-background 4s linear infinite;
```
Written as individual properties it would look like:
```css
animation-name: change-background;
animation-duration: 4s;
animation-timing-function: linear;
animation-repeat: infinite;
```
Where a transition takes a property, such as “background” or “all”


### Keyframes
A set of keyframes in CSS is a series of stops along the way through an animation. Each “keyframe” is a written as a percentage.

“Start at 0% of the way through with a blue background, then by 50% through be orange, and at 100% have a green background”
```css
@keyframes change-background {
0% {
background: blue;
}
50% {
background: orange;
}
100% {
    background: green;
}
}
```


### Prefixes
While this is becomeing less important, you may want to use the -webkit- prefix on the animation property. I won’t add it to examples, but it will be needed for your animations to work in browsers such as Safari.
In CodePen you can use the “Autoprefixer” option within the CSS settings. For local development, I use the Gulp version of Autoprefixer. Prefix Free is a decent alternative also.


### Homework



## Chapter 12 -  Animation properties
- **animation-delay** - Similar to transition-delay, we can use this property to make the animation wait before starting. This can be particularly useful in situations where there are multiple animations taking place.
  
- **animation-direction** - Animations normally begin at 0% and finish at 100%. Using animation-direction we use the values normal, reverse, alternate and alternate-reverse to control the direction.

- **animation-duration** - This is the length of the animation. Similar to transition-duration, this takes a value such as 1s for one second or 200ms for two hundred milliseconds.
  
- **animation-fill-mode** - By default, an animation will play and then the element returns to its normal state. Using animation-fill-mode we can have the animation “stick” at either the end or beginning state.
Using the value forwards tells the animation to finish and stay on the last keyframe. The value backwards returns to the first keyframe when the animation finishes.
An example of this is the bouncer animation on Hop.ie. The animation plays once and finishes on the last frame. This is using the value forwards.
- **animation-iteration-count** -This is the number of times the animation plays. By default it will play once.
You can specify a number, or “infinite” to have it loop forever.
- **animation-name** - The animation-name refers to the keyframes associated with the animation. For example, if the animation-name is set to “foo”, it would use a set of keyframes like:
```css
@keyframes foo {
...
}
```
- **animation-play-state** - If you ever need to pause or resume an animation, this property lets you do so.
It takes the values of running or paused, with the default being running. One
idea might be to set this value on an animation using JavaScript.
- **animation-timing-function** - This takes the same values the timing function property in transitions, but
behaves a little differently. While a timing function, such as ease-out applies to the entire transition, the timing function of an animation applies between each keyframe.
This means that the following keyframes would see the animation starting fast and slowing toward 50%, then picking up fast and slowing down before 100%.




### Using timing functions within keyframes
When you specify a timing function for an animation, the timing function applies to each keyframe of the animation.
This means that if you were to specify four keyframes, the timing function would apply to each. An ease-out function would slow down as it approached each keyframe.
For that reason we would usually define the timing function for animations as linear, and control the pacing on a per-keyframe basis:
```css
@keyframes my-animation {
0% {
...
animation-timing-function: linear;
}
50% {
...
animation-timing-function: ease-out;
}
}
```


### Homework



## Chapter 13 -  Keyframes in action
### Things to look out for
The first is an alternate syntax you may see, using the keywords from and to.
```css
@keyframes name {
from {
...
}
to {
...
}
}
```
While this is simple an alternate way of writing 0% and 100%, it can be simplerto understand and useful for simple animations.
You may have noticed that sometimes more than one percentage value is used on the same line. This is a way to have the animation pause for a while, or hold a particular state.
For example:
```css
@keyframes name {
0%, 20% {
opacity: 0;
}
100% {
opacity: 1;
}
}
```
This example will have the element start with an opacity of 0, and stay invisible until 20% through the animation, at which time it will then begin to animate
toward an opacity of 1.



### Example: Save button wiggle effect
```css
button {
animation: wiggle 2s linear infinite;
}
```

Next, we plan out what these keyframes are for the “wiggle” animation. Here’s
the result:
```css
@keyframes wiggle {
0%, 7% {
transform: rotateZ(0);
}
15% {
transform: rotateZ(-15deg);
}
20% {
transform: rotateZ(10deg);
}
25% {
transform: rotateZ(-10deg);
}
30% {
transform: rotateZ(6deg);
}
35% {
transform: rotateZ(-4deg);
}
40%, 100% {
transform: rotateZ(0);
}
}
```

### Homework



## Chapter 14 -  Multiple animations
In this chapter we’ll be looking at how we can make use of multiple sets of keyframes running at the same time.

### Traffic lights
There are times when we want multiple animations on a page to stay in sync, but at the same time each animation has its own timing. A good example that illustrates this is traffic lights
Here we have a simple (UK-style) traffic light pattern:
We have three lights, each with their own pattern of being off and on. We can
create this by giving each light their own animation.
```css
.red {
animation: red 10s linear infinite;
}
.amber {
animation: amber 10s linear infinite;
}
.green {
animation: green 10s linear infinite;
}
```
We have three animations, one for each light. Each animation lasts the same length of time so that when they loop, they won’t go out of sync. Next we need to plan the keyframes.

When creating this example I found it helpful to think of the lights as a grid. The animation happens from left to right, with each light being on or off at The grid is divided up into 5 columns. This means that we can deal with “chunks” of 20% and create sets of keyframes from these chunks.

```css 
@keyframes red {
0% {
background: black;
}
2%, 40% {
background-color: red;
}
42%, 100% {
background: black;
}
}

@keyframes amber {
0%, 20% {
background: black;
}
22%, 40% {
background: #FF7E00;
}
42%, 80% {
background: black;
}
82%, 100% {
background: #FF7E00;
}
}

@keyframes green {
0%, 40% {
background: black;
}
42%, 80% {
background: green;
}
82%, 100% {
background: black;
}
}
```



### Further reading
### Homework



## Chapter 15 -  Animation recap
### Homework challenge: Traffic lights
### Recap: Animations
### Putting them together
### Homework



## Chapter 16 -  Storytelling
### Heroes
### Example: Scrolling background
### Part 1: Background animation
### Part 2: Adding the hover transition
### Summary
### Homework



## Chapter 17 -  Star Wars
### Transform: Not an animation property
### Transform: scale(), translateZ() and rotateY()
### SVG, HTML and CSS
### Animating the Star and Wars
### Making it 3D 
### The Force Awakens
### Homework



## Chapter 18 -  Revealing content on scroll
### Wowjs
### Using Wowjs
### Adding “wow” classes
### Hiding and showing
### Using Animatecss
### Using Modernize
### Homework



## Chapter 19 -  Accessibility
### Make sure content is accessible
### Give control
### Allow for alternate inputs
### Confusion
### Don’t make me sick
### Accessibility is for everyone’s benefit
### Homework



## Chapter 20 -  Now you know CSS animation!
### CSS Animation cheatsheet
### Resources to bookmark 
### Other tools
### Next steps
