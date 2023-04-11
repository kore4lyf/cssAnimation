# CSS Transforms
CSS transforms allow you to move, rotate, scale, and skew elements.

## Browser Specific Prefixes
Some older browsers need specific prefixes (-ms- or -webkit-) to understand the 2D transform properties:

Example
```css
div {
  -ms-transform: rotate(20deg); /* IE 9 */
  -webkit-transform: rotate(20deg); /* Safari prior 9.0 */
  transform: rotate(20deg); /* Standard syntax */
}
```

## CSS 2D Transforms Methods
With the CSS transform property you can use the following 2D transformation methods:

- translate()
- rotate()
- scaleX()
- scaleY()
- scale()
- skewX()
- skewY()
- skew()
- matrix()

### The translate() Method
The translate() method moves an element from its current position (according to the parameters given for the X-axis and the Y-axis).

The following example moves the <div> element 50 pixels to the right, and 100 pixels down from its current position:

Example
```css
div {
  transform: translate(50px, 100px);
}
```