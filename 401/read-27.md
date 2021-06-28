## Describe use cases for useMemo() and useReducer()

* useMemo is a React hook that memorizes the output of a function. That is it. useMemo accepts two arguments: a function and a list of dependencies. useMemo will call the function and return its return value.

* useReducer is used to store and update states, just like the useState Hook. It accepts a reducer function as its first parameter and the initial state as the second.

## Why do custom hooks need the use prefix?

 * Custom Hooks are JavaScript functions whose names are prefixed with the word use. A custom Hook is a normal function but we hold them to a different standard. By adding the word use to the beginning, it lets us know that this function follows the rules of Hooks.


## What do custom hooks usually do?

Custom hooks allow us to have cleaner functional components, remove logic from the UI layer, and prevent code duplication by bringing common use cases to reusable hooks.


### Using any list of custom hooks, research and name one that you think will be useful in your applications

react-use-form-state is a hook that helps maintain the state in different parts of an app. This could be really useful, as this has been a challenge in the ToDo app.  


## Describe how a hook that fetches API data might work

First, we're going to import stuff we're going to use and create a function. The next step is to add a useState hook and to define the name of the state - in our case, that's data. Then, we define the function we'll use later on to update the state - setData

### Term 

* reducer : The useReducer is a hook I use sometimes to manage the state of the application. ... It acts as an alternate hook to the useState hook to manage complex state in your application. The useReducer hook uses the same concept as the reducers in Redux. It is basically a pure function, with no side-effects.


### When to Use Context
Context is designed to share data that can be considered “global” for a tree of React components, such as the current authenticated user, theme, or preferred language. For example, in the code below we manually thread through a “theme” prop in order to style the Button component:

```
class App extends React.Component {
  render() {
    return <Toolbar theme="dark" />;
  }
}

function Toolbar(props) {
  // The Toolbar component must take an extra "theme" prop
  // and pass it to the ThemedButton. This can become painful
  // if every single button in the app needs to know the theme
  // because it would have to be passed through all components.
  return (
    <div>
      <ThemedButton theme={props.theme} />
    </div>
  );
}

class ThemedButton extends React.Component {
  render() {
    return <Button theme={this.props.theme} />;
  }
}
```


```
// Context lets us pass a value deep into the component tree
// without explicitly threading it through every component.
// Create a context for the current theme (with "light" as the default).
const ThemeContext = React.createContext('light');

class App extends React.Component {
  render() {
    // Use a Provider to pass the current theme to the tree below.
    // Any component can read it, no matter how deep it is.
    // In this example, we're passing "dark" as the current value.
    return (
      <ThemeContext.Provider value="dark">
        <Toolbar />
      </ThemeContext.Provider>
    );
  }
}

// A component in the middle doesn't have to
// pass the theme down explicitly anymore.
function Toolbar() {
  return (
    <div>
      <ThemedButton />
    </div>
  );
}

class ThemedButton extends React.Component {
  // Assign a contextType to read the current theme context.
  // React will find the closest theme Provider above and use its value.
  // In this example, the current theme is "dark".
  static contextType = ThemeContext;
  render() {
    return <Button theme={this.context} />;
  }
}
```

## API
React.createContext
`const MyContext = React.createContext(defaultValue);`

Creates a Context object. When React renders a component that subscribes to this Context object it will read the current context value from the closest matching Provider above it in the tree.

The defaultValue argument is only used when a component does not have a matching Provider above it in the tree. This default value can be helpful for testing components in isolation without wrapping them. Note: passing undefined as a Provider value does not cause consuming components to use defaultValue.


## Context.Provider

`<MyContext.Provider value={/* some value */}>`


Every Context object comes with a Provider React component that allows consuming components to subscribe to context changes.

The Provider component accepts a value prop to be passed to consuming components that are descendants of this Provider. One Provider can be connected to many consumers. Providers can be nested to override values deeper within the tree.

All consumers that are descendants of a Provider will re-render whenever the Provider’s value prop changes. The propagation from Provider to its descendant consumers (including .contextType and useContext) is not subject to the shouldComponentUpdate method, so the consumer is updated even when an ancestor component skips an update.

Changes are determined by comparing the new and old values using the same algorithm as Object.is.

### REFERENCE 

* [context api](https://reactjs.org/docs/context.html)
* [hooks and context example](https://medium.com/swlh/snackbars-in-react-an-exercise-in-hooks-and-context-299b43fd2a2b)
* [react context links](https://github.com/diegohaz/awesome-react-context)
