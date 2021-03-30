# Javascript Templating
render client-side view templates by JSON data source.<br>
 The template engine then replaces variables and instances declared in a template file with actual values at runtime, and convert the template into an HTML file sent to the client.

# Flexbox properties 

### display
This defines a flex container; inline or block depending on the given value. It enables a flex context for all its direct children.

### flex-direction
the four possible values of flex-direction being shown: top to bottom, bottom to top, right to left, and left to right

This establishes the main-axis, thus defining the direction flex items are placed in the flex container. Flexbox is (aside from optional wrapping) a single-direction layout concept. Think of flex items as primarily laying out either in horizontal rows or vertical columns.

### example 
`.container {`
 ` flex-direction: row | row-reverse | column | column-reverse; }`


main axis;primary axis along which flex items are laid out <br>

main-start | main-end The flex items are placed within the container starting from main-start and going to main-end. main size A flex item’s width or height <br>
cross axis – The axis perpendicular to the main axis <br>
cross-start | cross-end – Flex lines are filled with items and placed into the container starting on the cross-start side of the flex container and going toward the cross-end side. cross size – The width or height of a flex item ..... etc <br>


## Prefixing Flexbox 
because the Flexbox spec has changed over time, it may give an error so , write in the new CSS