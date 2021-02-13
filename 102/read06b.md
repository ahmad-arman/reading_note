# css 
cascading style sheet 
use chang style page place text ,color , background color , height line , border ,padding , and margin 

CSS rule
contains two parts: a selector and a declaration.

![img](/assets/ugdagfl.png)


CSS declarations sit inside curly brackets and each is made up of two parts:
 a property and a value, separated by a colon. You can specify
several properties in one declaration, each separated by a semi-colon.

Properties : indicate the aspects
of the element you want to
change. For example, color, font,
width, height and border.

Values : specify the settings
you want to use for the chosen
properties

##  Using External CSS
how can I using exernal css 

1- `<link>`

 
The `<link>` element can be used
in an HTML document to tell the
browser where to find the CSS
file used to style the page.

2- href

This specifies the path to the
CSS file (which is often placed in
a folder called css or styles).

3- rel

This specifies the relationship
between the HTML page and
the file it is linked to. The value
should be stylesheet when
linking to a CSS file

## using internal css 

You can also include CSS rules
within an HTML page by placing
them inside a `<style>` element,
which usually sits inside the
`<head>` element of the page


When building a site with more
than one page, you should use
an external CSS style sheet. This:

1- Allows all pages to use the
same style rules (rather than
repeating them in each page).

2-Keeps the content separate
from how the page looks.

3- Means you can change the
styles used across all pages
by altering just one file
(rather than each individual
page).

# type of selctor 
1- Universal Selector

Applies to all elements in the
document 

  `* {}`

Targets all elements on the page

2-Type Selector

Matches element names

h1, h2, h3 {}

Targets the `<h1>, <h2> and <h3>`
elements

3-Class Selector

Matches an element whose
class attribute has a value that
matches the one specified after
the period (or full stop) symbol

`.note {}`
Targets any element whose class
attribute has a value of note

`p.note {}`
Targets only` <p> `elements
whose class attribute has a
value of note


4-ID Selector

Matches an element whose
id attribute has a value that
matches the one specified after
the pound or hash symbol

`#introduction {}`
Targets the element whose
id attribute has a value of
introduction

5-Child Selector

6-Descendant Selector

7-Adjacent Sibling Selector

8-General Sibling Selector

# Inheritance 

If you specify the font-family
or color properties on the
`<body>` element, they will apply
to most child elements. This is
because the value of the
font-family property is
inherited by child elements. It
saves you from having to apply
these properties to as many
elements (and results in simpler
style sheets).

## example 

![img](/assets/jjjdff.png)







# coloor
 we can determination the color by three way :

 1- RGB Values 
  
Values for red, green, and blue
are expressed as numbers
between 0 and 255.
rgb(102,205,170)
This color is made up of the
following values:
102 red
205 green
170 blue

For example: rgb(100,100,90)

 2-hex codes 

 Hex Codes
Hex values represent values
for red, green, and blue in
hexadecimal code.
#66cdaa
The value of the red, 102, is
expressed as 66 in hexadecimal
code. The 205 of the green is
expressed as cd and the 170 of
the blue equates to aa.

 For example: #ee3e80

 3-color names 

 Color Names
Colors are represented by
predefined names. However,
they are very limited in number.
MediumAquaMarine
There are 147 color names
supported by browsers (this
color is MediumAquaMarine).

 For example: DarkCyan

 ## Background Color
 can change  background-color like that : 

 ![img](/assets/pihghfgf.png)

 # color real 
 Every color on a computer screen is created by mixing amounts of red,
green, and blue. To find the color you want, you can use a color picker

# Contrast 

When picking foreground and background
colors, it is important to ensure that there is
enough contrast for the text to be legible

1- low contresr  

Text is harder to read when
there is low contrast between
background and foreground
colors

2- medium contreast 

Text is easier to read when
there is higher contrast between
background and foreground
colors

3- high contresr 

For long spans of text, reducing
the contrast a little bit improves
readability. 

# CSS 3: Opacity 
which allows you to
specify the opacity of an element
and any of its child elements.
The value is a number between
0.0 and 1.0 (so a value of 0.5
is 50% opacity and 0.15 is 15%
opacity).

# CSS 3: HSL Colors
intuitive
way to specify colors using hue, saturation,
and lightness values.

1- Hue

 is the colloquial idea of
color. In HSL colors, hue is often
represented as a color circle
where the angle represents the
color values
from 0 to 360.

2-  saturation

 is the amount of
gray in a color. Saturation is
represented as a percentage.
100% is full saturation and 0%
is a shade of gray

3- Lightness
 is the amount of
white (lightness) or black
(darkness) in a color. Lightness
is represented as a percentage.
0% lightness is black, 100%
lightness is white, and 50%
lightness is normal.

# CSS 3: HSL & HSLA

hue

This is expressed as an angle
(between 0 and 360 degrees).

saturation

This is expressed as a
percentage.

lightness

This is expre
ssed as a
percentage with 0% being white,
50% being normal, and 100%
being black.

The hsla color property allows
you to specify color properties
using hue, saturation, and
lightness as above, and adds a
fourth value which represents
transparency (just like the rgba
property).

The a stands for:
alpha
This is expressed as a
number between 0 and 1.0.
For example, 0.5 represents
50% transparency, and 0.75
represents 75% transparency