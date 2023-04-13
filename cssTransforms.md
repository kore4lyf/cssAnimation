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

### CSS 2D Transforms Methods
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

#### The translate() Method
The translate() method moves an element from its current position (according to the parameters given for the X-axis and the Y-axis).

The following example moves the `<div>` element 50 pixels to the right, and 100 pixels down from its current position:

Example
```css
div {
  transform: translate(50px, 100px);
}
```


#### The rotate() Method
The rotate() method rotates an element clockwise or counter-clockwise according to a given degree.

The following example rotates the `<div>` element clockwise with 20 degrees:

Example
```css
div {
  transform: rotate(20deg);
}
```

Using negative values will rotate the element counter-clockwise.

The following example rotates the  `<div>` element counter-clockwise with 20 degrees:

Example
```css
div {
  transform: rotate(-20deg);
}
```

#### The scale() Method
The scale() method increases or decreases the size of an element (according to the parameters given for the width and height).

The following example increases the `<div>` element to be two times of its original width, and three times of its original height: 

Example
```css
div {
  transform: scale(2, 3);
}
```

The following example decreases the `<div>` element to be half of its original width and height: 

Example
```css
div {
  transform: scale(0.5, 0.5);
}
```


#### The scaleX() Method
The scaleX() method increases or decreases the width of an element.

The following example increases the `<div>` element to be two times of its original width: 

Example
```css
div {
  transform: scaleX(2);
}
```
The following example decreases the <div> element to be half of its original width: 

Example
```css
div {
  transform: scaleX(0.5);
}
```



#### The scaleY() Method
The scaleY() method increases or decreases the height of an element.

The following example increases the `<div>` element to be three times of its original height: 

Example
```css
div {
  transform: scaleY(3);
}
```



#### The skewX() Method
The skewX() method skews an element along the X-axis by the given angle.

The following example skews the `<div>` element 20 degrees along the X-axis:

Example
```css
div {
  transform: skewX(20deg);
}
```



#### The skewY() Method
The skewY() method skews an element along the Y-axis by the given angle.

The following example skews the `<div>` element 20 degrees along the Y-axis:

Example
```css
div {
  transform: skewY(20deg);
}
```



#### The skew() Method
The skew() method skews an element along the X and Y-axis by the given angles.

The following example skews the `<div>` element 20 degrees along the X-axis, and 10 degrees along the Y-axis:

Example
```css
div {
  transform: skew(20deg, 10deg);
}
```
f the second parameter is not specified, it has a zero value. So, the following example skews the `<div>` element 20 degrees along the X-axis:

Example
```css
div {
  transform: skew(20deg);
}
```



#### The matrix() Method
Rotate
The matrix() method combines all the 2D transform methods into one.

The matrix() method take six parameters, containing mathematic functions, which allows you to rotate, scale, move (translate), and skew elements.

The parameters are as follow: matrix(scaleX(),skewY(),skewX(),scaleY(),translateX(),translateY())

Example
```css
div {
  transform: matrix(1, -0.3, 0, 1, 0, 0);
}
```







## CSS 3D Transforms


### Browser Specific Prefixes
Some older browsers need specific prefixes (-webkit-) to understand the 3D transform properties:

Example
```css
#myDiv {
  -webkit-transform: rotateY(130deg); /* Safari prior 9.0 */
  transform: rotateY(130deg); /* Standard syntax */
}
```

### CSS 3D Transforms Methods
With the CSS transform property you can use the following 3D transformation methods:

- rotateX()
- rotateY()
- rotateZ()

#### The rotateX() Method
The rotateX() method rotates an element around its X-axis at a given degree:

Example
```css
#myDiv {
  transform: rotateX(150deg);
}
```

#### The rotateZ() Method
The rotateZ() method rotates an element around its Z-axis at a given degree:

Example
```css
#myDiv {
  transform: rotateZ(90deg);
}
```


#### CSS Transform Properties
The following table lists all the 3D transform properties:

| Property | Description |
| :--- | :--- |
| transform	| Applies a 2D or 3D transformation to an element |
| transform-origin | Allows you to change the position on transformed elements |
| transform-style | Specifies how nested elements are rendered in 3D space |
| perspective | Specifies the perspective on how 3D elements are viewed |
| perspective-origin | Specifies the bottom position of 3D elements |
| backface-visibility | Defines whether or not an element should be visible when not facing the screen |


##### CSS transform-origin Property
Set a rotated element's base placement:
```css
div {
  transform: rotate(45deg);
  transform-origin: 20% 40%;
}
```

###### CSS Syntax
```css
transform-origin: x-axis y-axis z-axis|initial|inherit;
```

###### Property Values
| Property Value | Description |
| :--- | :--- |
| x-axis | Defines where the view is placed at the x-axis. Possible values: left, center, right, length, % |
| y-axis | Defines where the view is placed at the y-axis. Possible values: top, center, bottom, length, % |
| z-axis | Defines where the view is placed at the z-axis (for 3D transformations). Possible values: length |


##### CSS transform-style Property
The transform-style property specifies how nested elements are rendered in 3D space.

Example
Let the transformed child elements preserve the 3D transformations:
```css
div {
  transform: rotateY(60deg);
  transform-style: preserve-3d;
}
```


###### CSS Syntax
```css
transform-style: flat|preserve-3d|initial|inherit;
```

###### Property Values
| Property Value | Description |
| :--- | :--- |
| flat | Specifies that child elements will NOT preserve its 3D position. This is default |
| preserve-3d | Specifies that child elements will preserve its 3D position |





##### CSS perspective Property
Give a 3D-positioned element some perspective:
```css
#div1 {
  perspective: 100px;
}
```
The perspective property is used to give a 3D-positioned element some perspective.

The perspective property defines how far the object is away from the user. So, a lower value will result in a more intensive 3D effect than a higher value.

When defining the perspective property for an element, it is the CHILD elements that get the perspective view, NOT the element itself.


##### CSS perspective-origin Property
The perspective-origin property defines at from which position the user is looking at the 3D-positioned element.

Example
Define at from which position the user is looking at the 3D-positioned element:
```css
#div1 {
  perspective: 100px;
  perspective-origin: left;
}
```

###### CSS Syntax
```css
perspective-origin: x-axis y-axis|initial|inherit;
```

###### x-axis
Possible values: left, center, right, length, %
Default value: 50%

###### y-axis
Possible values: left, center, right, length, %
Default value: 50%


##### CSS backface-visibility Property
The backface-visibility property defines whether or not the back face of an element should be visible when facing the user.

Example
Hide and show the back face of two rotated `<div>` elements:
```css
#div1 {
  backface-visibility: hidden;
}

#div2 {
  backface-visibility: visible;
}
```


#### CSS 3D Transform Methods
| Function	| Description |
| :--- | :--- |
| matrix3d
(n,n,n,n,n,n,n,n,n,n,n,n,n,n,n,n) | Defines a 3D transformation, using a 4x4 matrix of 16 values |
| translate3d(x,y,z) | Defines a 3D translation
| translateX(x)	| Defines a 3D translation, using only the value for the X-axis |
| translateY(y)	| Defines a 3D translation, using only the value for the Y-axis |
| translateZ(z)	| Defines a 3D translation, using only the value for the Z-axis |
| scale3d(x,y,z) |Defines a 3D scale transformation
| scaleX(x) | Defines a 3D scale transformation by giving a value for the X-axis |
| scaleY(y)	| Defines a 3D scale transformation by giving a value for the Y-axis |
| scaleZ(z)	| Defines a 3D scale transformation by giving a value for the Z-axis |
| rotate3d(x,y,z,angle)	| Defines a 3D rotation |
| rotateX(angle) | Defines a 3D rotation along the X-axis |
| rotateY(angle) | Defines a 3D rotation along the Y-axis |
| rotateZ(angle) | Defines a 3D rotation along the Z-axis |
| perspective(n) | Defines a perspective view for a 3D transformed element | 
