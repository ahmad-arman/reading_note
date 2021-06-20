Name 5 Javascript UI Frameworks (other than React)?<br>
1-  Angular<br>
2-   Vue.js<br>
3-   jQuery<br>
4-   Backbone.js<br>
5-   Meteor<br>
What’s the difference between a framework and a library? <br>
The key difference between a library and a framework is "Inversion of Control".
 
When you call a method from a library, you are in control. But with a framework, the control is inverted: the framework calls you.

## Terms 

1-  Rendering :  is a process used in web development that turns website code into the interactive pages users see when they visit a website.

2- Templates :  refers to the client side data binding method implemented with the JavaScript language. Popular JavaScript templating languages are: AngularJS, Backbone.js, Ember.js, Handlebars.js, and Mustache.js. The templating engine is responsible for connecting to the data model, processing the code specified in the source templates, and directing the output to a specific pipeline, text file, or stream.<br>
3-State :The state is an instance of React Component Class can be defined as an object of a set of observable properties that control the behavior of the component. In other words, the State of a component is an object that holds some information that may change over the lifetime of the component

# React 
React is a JavaScript library, and so we’ll assume you have a basic understanding of the JavaScript language.


The smallest React example looks like this:

```
ReactDOM.render(
  <h1>Hello, world!</h1>,
  document.getElementById('root')
);
```

### JSX 

Embedding Expressions in JSX

In the example below, we declare a variable called name and then use it inside JSX by wrapping it in curly braces:



```
const name = 'Josh Perez';
const element = <h1>Hello, {name}</h1>;

ReactDOM.render(
  element,
  document.getElementById('root')
);
```

In the example below, we embed the result of calling a JavaScript function, formatName(user), into an `<h1> `element.




```
function formatName(user) {
  return user.firstName + ' ' + user.lastName;
}

const user = {
  firstName: 'Harper',
  lastName: 'Perez'
};

const element = (
  <h1>
    Hello, {formatName(user)}!
  </h1>
);

ReactDOM.render(
  element,
  document.getElementById('root')
);
```

This means that you can use JSX inside of if statements and for loops, assign it to variables, accept it as arguments, and return it from functions:

```
function getGreeting(user) {
  if (user) {
    return <h1>Hello, {formatName(user)}!</h1>;
  }
  return <h1>Hello, Stranger.</h1>;
}
```


Specifying Attributes with JSX <br>
You may use quotes to specify string literals as attributes:

`const element = <div tabIndex="0"></div>;`

You may also use curly braces to embed a JavaScript expression in an attribute:

`const element = <img src={user.avatarUrl}></img>;`


Babel compiles JSX down to React.createElement() calls.

```
const element = (
  <h1 className="greeting">
    Hello, world!
  </h1>
);
```

```
const element = React.createElement(
  'h1',
  {className: 'greeting'},
  'Hello, world!'
);
```

```
// Note: this structure is simplified
const element = {
  type: 'h1',
  props: {
    className: 'greeting',
    children: 'Hello, world!'
  }
};
```

To render a React element into a root DOM node, pass both to ReactDOM.render():

```
const element = <h1>Hello, world</h1>;
ReactDOM.render(element, document.getElementById('root'));
```

the only way to update the UI is to create a new element, and pass it to ReactDOM.render()

```
function tick() {
  const element = (
    <div>
      <h1>Hello, world!</h1>
      <h2>It is {new Date().toLocaleTimeString()}.</h2>
    </div>
  );
  ReactDOM.render(element, document.getElementById('root'));
}

setInterval(tick, 1000);
```
It calls ReactDOM.render() every second from a setInterval() callback.

## REFERENCE : 

[react](https://reactjs.org/docs/rendering-elements.html)

[sass cheatsheet](https://devhints.io/sass)

[react cheatsheet](https://devhints.io/react)

[another react cheatsheet](https://reactcheatsheet.com/)
