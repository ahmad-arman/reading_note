### What are the advantages of storing tokens in “Cookies” vs “Local Storage”

1- Cookies have an expiry date, unlike local storage
2- Cookies are automatically saved, sent, and removed by the browser.
3- cookies can be accessed from both the back-end (req.headers.cookie) and front-end but the local   storage Data is only accessed from the local browser. The server can’t access local storage unless a  request been send (POST or GET)
4- Cookies have 4094 bytes per cookie but local storage 5 MB per domain


### Explain 3rd party cookies.

Third-party cookies are cookies that are set by a website other than the one you are currently on. For example, you can have a "Like" button on your website which will store a cookie on a visitor's computer, that cookie can later be accessed by Facebook to identify visitors and see which websites they visited.


### How do pixel tags work?

 is a graphic with dimensions of 1x1 pixels that is loaded when a user visits a webpage or opens an email. ... The tracking pixel URL is the memory location on the server. When the user visits a website, the image with the tag is loaded from this server


# Term 

* cookies: Cookies are data, stored in small text files, on your computer. When a web server has sent a web page to a browser, the connection is shut down, and the server forgets everything about the user. ... When a user visits a web page, his/her name can be stored in a cookie

* authorizationis the process of giving someone permission to do or have something. ... Thus, authorization is sometimes seen as both the preliminary setting up of permissions by a system administrator and the actual checking of the permission values that have been set up when a user is getting access.

* access control  Component of data security that dictates who is allowed to access and use company information and resources. Through authentication and authorization, access control policies make sure users are who they say they are and that they have appropriate access to company data.

* conditional rendering  is a term to describe the ability to render different user interface (UI) markup if a condition is true or false. In React, it allows us to render different elements or components based on a condition.



### REDUX 

Redux provides a solid, stable, and mature solution to managing state in your React application. Through a handful of small, useful patterns, Redux can transform your application from a total mess of confusing and scattered state, into a delightfully organized, easy to understand modern JavaScript powerhouse.

The principles of Redux aren't new, but they are packaged and presented for you in an easy to use a library that not only elevates your applications but also improves your general understanding of building JavaScript UIs.

In this course, Dan Abramov will show you the fundamentals of Redux, so that you can start using it to simplify your applications.

### What is Redux? 

Redux takes away some of the hassles faced with state management in large applications. It provides you with a great developer experience, and makes sure that the testability of your app isn’t sacrificed for any of those.

As you develop React applications, you may find that keeping all your state in a top-level component is no longer sufficient for you.

You may also have a lot of data changing in your application over time.


### Why use Redux? 

Redux itself is a standalone library that can be used with any UI layer or framework, including React, Angular, Vue, Ember, and vanilla JS. Although Redux and React are commonly used together, they are independent of each other.

If you are using Redux with any kind of UI framework, you will normally use a "UI binding" library to tie Redux together with your UI framework, rather than directly interacting with the store from your UI code.

React Redux is the official Redux UI binding library for React. If you are using Redux and React together, you should also use React Redux to bind these two libraries.

### Integrating Redux with a UI#
Using Redux with any UI layer requires the same consistent set of steps:

1- Create a Redux store <br>
2-Subscribe to updates <br>
3-Inside the subscription callback: <br>
 a -Get the current store state <br>
 b- Extract the data needed by this piece of UI <br>
 c-Update the UI with the data <br>
4- If necessary, render the UI with initial state <br>
5- Respond to UI inputs by dispatching Redux actions <br>
While it is possible to write this logic by hand, doing so would become very repetitive. In addition, optimizing UI performance would require complicated logic.

The process of subscribing to the store, checking for updated data, and triggering a re-render can be made more generic and reusable. A UI binding library like React Redux handles the store interaction logic, so you don't have to write that code yourself.




#### REFERENCE

* [  Dan Abramov Redux Tutorials](https://egghead.io/courses/fundamentals-of-redux-course-from-dan-abramov-bd5cc867)

* [worlds easiest guide to redux](https://www.freecodecamp.org/news/understanding-redux-the-worlds-easiest-guide-to-beginning-redux-c695f45546f6/)
* [testing reducers](https://medium.com/@netxm/testing-redux-reducers-with-jest-6653abbfe3e1 )
 * [Redux Docs](https://redux.js.org/) 