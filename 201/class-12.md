# Chart.js
Chart.js can be used with ES6 modules, plain JavaScript and module loaders.

## Chart type
The types of charts that you can use:<br>
1-Line<br>
2-Bar<br>
3-Radar<br>
4-Doughnut and Pie<br>
5-Polar area<br>
6-Bubble<br>
7-Scatter<br>




![img](https://steemitimages.com/640x0/https://res.cloudinary.com/hpiynhbhq/image/upload/v1514129984/ccmoj2hea1idle17ywfx.png)

# The canvas element 

`<canvas id="tutorial" width="150" height="150"></canvas>`<br>
At first sight a `<canvas> `looks like the `<img>` element, with the only clear difference being that it doesn't have the src and alt attributes. Indeed, the `<canvas>` element has only two attributes, width and height.

## Required canvas tag 
the `<canvas>` element requires the closing tag (`</canvas>`). If this tag is not present, the rest of the document would be considered the fallback content and wouldn't be displayed.

##  The rendering context

`var canvas = document.getElementById('tutorial');` <br>
`var ctx = canvas.getContext('2d');`<br>
The first line in the script retrieves the node in the DOM representing the` <canvas> `element by calling the document.getElementById() method. Once you have the element node, you can access the drawing context using its getContext() method.

## Checking for support 

The fallback content is displayed in browsers which do not support `<canvas>.` Scripts can also check for support programmatically by testing for the presence of the getContext() method.

`(var canvas = document.getElementById('tutorial');`

``if (canvas.getContext) {``
 `` var ctx = canvas.getContext('2d');``
 `` // drawing code here``
``} else {``
  ``// canvas-unsupported code here``
``})``

## Example 
![img](../assets/hhjrjreuir.png)


## Rectangular shape example 

![img](../assets/jjrkrhgk.png)

![img](../assets/jfhfdhk.png)

## Colors 
Up until now we have only seen methods of the drawing context. If we want to apply colors to a shape, there are two important properties we can use: fillStyle and strokeStyle.

fillStyle = color <br>
Sets the style used when filling shapes.<br>
strokeStyle = color<br>
Sets the style for shapes' outlines. <br>

for example :

ctx.fillStyle = 'orange'; <br>
ctx.fillStyle = '#FFA500';<br>
ctx.fillStyle = 'rgb(255, 165, 0)';<br>
ctx.fillStyle = 'rgba(255, 165, 0, 1)';<br>


## A fillText example
The text is filled using the current fillStyle.

![img](../assets/sjfhkfhgk.png)

## A strokeText example
The text is filled using the current strokeStyle.

![img](../assets/sjfhkfhgk.png)
