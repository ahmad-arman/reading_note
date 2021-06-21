## Can a parent component access the state of a child component?

yes

## What can be passed along in a prop variable?

all the data from state
## How can a child component “know” the state of another component?

use props


## Term

* component props : Props are arguments passed into React components.
React Props are like function arguments in JavaScript and attributes in HTML.
To send props into a component, use the same syntax as HTML attributes:

* component state : The state is an instance of React Component Class can be defined as an object of a set of observable properties that control the behavior of the component. In other words, the State of a component is an object that holds some information that may change over the lifetime of the component.


* application state : . State is a JavaScript object. It stores a component's dynamic data and determines the component's behavior. ... State helps in keeping the data of different components in sync since each state update will re-render all relevant components



## react basics recap 

### Mounting
Since class-based components are classes, hence the name, the first method that runs is the constructor method. Typically, the constructor is where you would initialize component state.

### Updating
This phase is triggered every time state or props change. Like in mounting, getDerivedStateFromProps is called (but no constructor this time!).

### Unmounting
Our component lived a good life, but all good things must come to an end. The unmounting phase is that last stage of the component lifecycle. When you remove a component from the DOM, React runs `componentWillUnmount` right before it gets removed. You should use this method to clean up any open connections such as WebSockets or intervals.

### Other Lifecycle Methods
Before we move onto the next topic, let’s briefly talk about `forceUpdate` and `getDerivedStateFromError.`

`forceUpdate` is a method that directly causes a re-render. While there may be a few use cases for it, it should typically be avoided.

`getDerivedStateFromError `on the other hand is a lifecycle method that isn’t directly part of the component lifecycle. In the event of an error in a component, `getDerivedStateFromError` runs and you can update state to reflect that an error occurred. Use this method copiously.


### What even is ‘children’?
The React docs say that you can use props.children on components that represent ‘generic boxes’ and that ‘don’t know their children ahead of time’. For me, that didn’t really clear things up. I’m sure for some, that definition makes perfect sense but it didn’t for me.
My simple explanation of what this.props.children does is that it is used to display whatever you include between the opening and closing tags when invoking a component.

### Containment
Some components don’t know their children ahead of time. This is especially common for components like Sidebar or Dialog that represent generic “boxes”.

We recommend that such components use the special children prop to pass children elements directly into their output:

```
function FancyBorder(props) {
  return (
    <div className={'FancyBorder FancyBorder-' + props.color}>
      {props.children}
    </div>
  );
}
```

This lets other components pass arbitrary children to them by nesting the JSX:
```

function WelcomeDialog() {
  return (
    <FancyBorder color="blue">
      <h1 className="Dialog-title">
        Welcome
      </h1>
      <p className="Dialog-message">
        Thank you for visiting our spacecraft!
      </p>
    </FancyBorder>
  );
}

```
## REFERENCE 
[react basics recap](https://www.freecodecamp.org/news/these-are-the-concepts-you-should-know-in-react-js-after-you-learn-the-basics-ee1d2f4b8030/) <br />
[props.children](https://codeburst.io/a-quick-intro-to-reacts-props-children-cb3d2fce4891) <br>
[composition vs inheritance](https://reactjs.org/docs/composition-vs-inheritance.html) <br />
[react testing library api example](https://testing-library.com/docs/react-testing-library/example-intro/) <br />

[react-if component](https://www.npmjs.com/package/react-if)

[react-testing-library-async](https://testing-library.com/docs/dom-testing-library/api-async/)