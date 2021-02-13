# What I need when I want work web pages
 1- HTML (for structure) 
 
 2- CSS (for presentation )

 3- JS  ( for interactive and dynamic with users )

# how the web work 
1- when concet with web , (isp) internat Service Provider then write name domain or address page 

2- your computer will conceted with (DNS) domain name system , every computer has unique IP numder on web 

3-The unique number that the DNS server returns to your computer allows your browser to contact the web server

4- The web server then sends the page you requested back to your web browser.

# HTML 
HTML : Heyper text Markup Language. Html : it help software developer to change structure documents to help peaple in reading clearly.
 
## HTML PAGE 
  content from two main things  :
   1- head (we have here title ,people can not see this tag, that appear in title bar )

   2- body (we have here shape page , people can see every thing here)

##  when start write code with Html you must know some things : 

  1- <  > that is mean start tag    
  
  2- </  >  that is mean close tag 

## look how can I write code :
  `<!Doctype html >`
 `<html>`

  `<head>`

   `<title> title bar  </title>`

  `</head> `

  `<body> `

   `<h1>title the page  </h1>`

  `<p> you can write here ang thing      </p>`

  `</body>`

 `</html>`  
 
## Attributes Tell Us More About Elements 
They appear on the opening tag of the element and are made up of two parts: a name and a value, separated by an equals sign.

## HTML Version
 The html version that will use it is : HTML5,so when use HTML code you must write befor anything

  `<!DOCTYBE html>`

 That is  mean is tall browser which version html page is useing. 

## Comments Html  

  1- `<!-- here you can add comment  -->` 
  
  that is mean when you want add comment to your code that will not display in user's browser 
  That will help new devloper to understand code clearly and can add some link as email to can call with past devloper and all of thess not appear to user's browser.

## ID Attribute 

  is used to specify a unique id for an HTML element.
  You cannot have more than one element with the same id in an HTML document.

  `<p id="ahmd" > you can write ang think here</p>`

##  Class Attribute  
 A method for identifying multiple items On it is different from Other items on the page.  

 `<p class="ahm" > you can write here any thing </p>`


##  Block Elements 
 are the elements that will  appear to start on a new line in the browser window.

  Examples of block elements are
 `<h1>, <p>, <ul>, and <li>`.

## Inline Elements :
Inline elements will always appear to continue on the same line as their neighbouring elements.

Examples of inline elements are
`<a>, <b>, <em>, and <img>`.

##  Grouping Text & Elements In a Block

The `<div>` element allows you to group a set of elements together in one block-level box. For example, you might create a <div> element to contain all of the elements for the headerof your site .

##  Grouping Text & Elements Inline :
`<span>`
The `<span>` element acts like an inline equivalent of the `<div>` element. It is used to either:

1. Contain a section of text where there is no other suitable element to differentiate it from its surrounding text

2. Contain a number of inline elements 

The most common reason why people use `<span>` elements is so that they can control the appearance of the content of these elements using CSS. You will usually see that a class or id attribute is used with `<span>` elements:

●● To explain the purpose of this `<span>` element

●● So that CSS styles can be applied to elements that have specific values for these attributes

## `<IFrames>`:

use to Put a map on the page .that will need some element :

1- src :

 use to defined the link page to show in the frame
2- height :

use to defined the height of the iframe in pixels.

3- width :

use to defined the width of the iframe in pixels.

## The `< meta >` 

tag allows you to put all kinds of information about your web page

## HTML5 Layout
HTML5 : is introducing a new set of elements that help define the structure of a page, The new elements provide clearer code (compared with using multiple `<div>` elements)

## `<header>` & `<footer>` 
 header : used element put on the top of page on the site 

 footer : used element put on the botton of page on the site  

## `<nav>` 
  navigation : is contain the major navigational
blocks on the site

## `<article>` 
  it is element acts can put any section of a
page such as (`<hgroub>`,`<figure>`, `<figcaption>`)

## <aside>
depending if inside `<artical>`element or out side `<artiacl>`

inside element artical : that is should contain on 
information that is related to the
article but not primary 

outside element artical :  it work as a container
for content that is related to the entire page

## `<section>` 

We should place all things under each section as appropriate

## `<hgroup>`
 it is a set of groubes that content the title`<h1><h2><hn>` 

## `<figure> <figcaption>` 
 that used to contain any content that is referenced from the main flow of an article such as : 

1- Images

2- Videos

3- Graphs

4- Diagrams

5- Code samples

The `<figure>` element should
also contain a `<figcaption>`
element which provides a text
decription for the content of
the `<figure>` element.

##  Process & Design

when we work any website we must know the important point who is the target audience? The website will be different in design according to the users

 also you must answer for question why the users are visiting your website if you have in your web site  motivations users and hit their goals will be sucsses website

Also when start desgin your website page you must to You should take care of the site map, which will greatly help your website succeed ,This image example map site 


and also we need a care about WireFrames that you can
ensure that all of the information
that needs to be on a page is
included. 

 

 Also Visual hierarchy is an important to care about because  will help you to communicate with the users on the website 


# javascript 
java script langauge is a text-based programming langauge , give web page dymanic and interactive that engage users

## How javascript do interactive 
 1-access content 

  can java script to select text , element frome Html page 

2-modify content 

  can java script to remove ,add  text , element frome Html page

3- program rules  You can defined a set of steps for

the browser to follow (like a recipe )

 4-rect to event (You can defined  that a script should run

when a specific event has occurred.

## Example

1- Slidesshows

React : Script triggered when the page loads

Access: Get each slide from the slideshow

Modify: Only show the first slide (hide others)

Program: Set a timer: when to show next slide

Modify: Change which slide is shown

React: When user clicks button for diffe rent sl ide

Program: Determine which slide to show

Modify: Show the requested slide

 To write a script, you need to first
state your goal

##  To write a script you need 

1- defined the goak

2- desgin the script

3-code each step 

# Expression 
 ther are two type expression : 

 1-  assign a value to variable  
 var color = " blue ";

 The value of color is now bule 

 2-use two or more values to return assign a value 

 var = 2*2;

The value of area is now 4

# operators
1- assigment opertors 

Assign a value to a variable

color = 'beige';

2- arithmetic operators

Perform basic math
area = 3 * 2;

## JavaScript contains the following mathematical operators
 which you can use with numbers
You may remember some from math class 

![img](/assets/44.png)

## using aritmethic operators
The numbers do not need to be written explicitly into the code 

![img](/assets/666666.png)

##  string operator
that is use for symbol without number 

 example : <br>
 var firstName = 'ahmad ' ;

var lastName = ' arman' ;

var ful l Name = firstName + lastName

## mix with string and number operator
if put number inside single cotation the program consist this number is string ,whitout single cotation program
consist this number is number 

![img](/assets/56.png)


## Each object can have its own:

• Properties

Each property has a name and a value, and each of
these name/value pairs tells you something about
each individual instance of the object.

• Events

There are common ways in which people interact
with each type of object. For example, in a car a
driver will typically use at least two pedals

• Methods

Methods typically represent how people (or other
things) interact with an object in the real world.

## PUTTING IT ALL TOGETHER
Computers use data to create models of things in the real world.
The events, methods, and properties of an object all relate to each other:
Events can trigger methods, and methods can retrieve or update an
object's properties.