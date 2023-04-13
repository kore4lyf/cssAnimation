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
They’re usually triggered by an action such hovering over an element, or adding
or removing a class using JavaScript.
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
When writing CSS, we can often summarise multiple properties into one in a
shorthand property. For example, padding written as shorthand might look like
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
While you can use transitions on positioning, size, colour, border, background-
position and many others, there are some that cannot be transitioned. The
font-family cannot be transitioned, as this would mean trying to generate frames
between two very different font images.
Background images created with CSS, such as generated gradients, cannot
have their properties animated. This would mean the browser recreating the
background image with each frame of animation and so is not supported.
However you can animate things like opacity and background position. By
moving background images around or hiding them you can create interesting
effects.


### Homework



## Chapter 8 - Timing functions 30
### Linear
### Ease-in
### Ease-out
### Ease-in-out
### Cubic-bezier
### Steps
### More examples
### Homework



## Chapter 9 - Multiple transitions
### Example 1: Fancy button
### Example 2: Background reveal
### Multiple transitions on a single element
### Homework



## Chapter 10 - Transitions and JavaScript
### Add or remove classes
### Controlling transitions with JavaScript
### Let’s recap
### Homework



## Chapter 11 -  Animations in action
### A symbiotic relationship
### The animation property
### Keyframes
### Prefixes
### Homework



## Chapter 12 -  Animation properties
### Using timing functions within keyframes
### Homework



## Chapter 13 -  Keyframes in action
### Things to look out for
### Example: Save button wiggle effect
### Homework



## Chapter 14 -  Multiple animations
### Traffic lights
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
