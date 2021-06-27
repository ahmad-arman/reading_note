#### What does a component’s lifecycle refer to?

 lifecycle of a component can be defined as the series of methods that are invoked in different stages of the component's existence. ... Mounting: Mounting is the stage of rendering the JSX returned by the render method itself.

#### Why do you sometimes need to “wrap” functions in useCallback when called from within useEffect

useCallback will help in avoiding regeneration of functions when the functional component re-renders. However there isn't much of a performance difference caused by recreation of functions. You are specifying a function as a dependency to useEffect 

#### Why are functional components preferred over class components?
Functional component are much easier to read and test because they are plain JavaScript functions without state or lifecycle-hooks. You end up with less code. They help you to use best practices.

#### What is wrong with the following code?

`useEffect` should only be used with the count is changed in the code above, so it does not make sense for it to be in a `for` loop. `useEffect` should be outside of the `for` loop in this example.


##  Terms 

* state hook : A Hook is a special function that lets you “hook into” React features. For example, useState is a Hook that lets you add React state to function components. <br>

* effect hook :  lets you perform side effects in function components: import React, { useState, useEffect } from 'react'; function Example() { const [count, setCount] = useState(0); // Similar to componentDidMount and componentDidUpdate: useEffect(() => { // Update the document title using the browser API document.

* reducer hook : is a hook I use sometimes to manage the state of the application. ... It acts as an alternate hook to the useState hook to manage complex state in your application. The useReducer hook uses the same concept as the reducers in Redux. It is basically a pure function, with no side-effects.


### use effect 
useEffect tells React that our component needs to do something after the component renders. It runs after the first render and after every update. In my previous articles, I only talk about side effects WITHOUT cleanup, so I would like to cover really quickly how to allow a functional component to have a side effect WITH cleanup.

Below is an example of how useEffect can run without any cleanup:

 ```   useEffect(() => {
      document.title = `You clicked ${count} times`;
    }); 
```

If you do need cleanup to run, you can return a function from useEffect. This is optional and it allows you to run some code after your effect and before any new effect runs. A situation where you subscribe to something may need an unsubscribe as part of the effects cleanup process. React will perform this cleanup on unmount.


 ``` useEffect(() => {
      console.log("Subscribe to Something);
      return function cleanup() {
        console.log("Unsubscribe to Something);
      };
    });
```

The effect above will run on every render more than one time. React cleans up effects from the previous render before running the effects of the next render, and this should be noted. For an explanation on why Hooks run on each update, check out the ReactJS Docs. Remember though, this behavior can be opted out of if it causes performance issues.


We can also optimize performance by skipping effects with an optional argument. For instance, maybe we don't want to run the subscribe/unsubscribe effect unless some id has changed. Check out the example below to understand how this can be done, it's fairly simple!
```
    useEffect(() => {
      console.log("Subscribe to Something);
      return () => {
        console.log("Unsubscribe to Something);
      };
    }, [props.something.id]); // only if something.id changes
```

## useReducer 

`const [state, dispatch] = useReducer(reducer, initialArg, init); ` 

useReducer is usually preferable to useState when you have complex state logic that involves multiple sub-values or when the next state depends on the previous one. useReducer also lets you optimize performance for components that trigger deep updates because you can pass dispatch down instead of callbacks.


### useToggle
Basically, what this hook does is that, it takes a parameter with value true or false and toggles that value to opposite. It's useful when we want to take some action into it's opposite action, for example: show and hide modal, show more/show less text, open/close side menu.

```
import { useCallback, useState } from 'react';
// Usage
function App() {
    // Call the hook which returns, current value and the toggler function
    const [isTextChanged, setIsTextChanged] = useToggle();
    
    return (
        <button onClick={setIsTextChanged}>{isTextChanged ? 'Toggled' : 'Click to Toggle'}</button>
    );
}
// Hook
// Parameter is the boolean, with default "false" value
const useToggle = (initialState = false) => {
    // Initialize the state
    const [state, setState] = useState(initialState);
    
    // Define and memorize toggler function in case we pass down the comopnent,
    // This function change the boolean value to it's opposite value
    const toggle = useCallback(() => setState(state => !state), []);
    
    return [state, toggle]
}
```

#### REFERENCE 

* [custom hooks - all you need to know](https://www.telerik.com/kendo-react-ui/react-hooks-guide/#toc-custom-react-hooks)
* [async hooks](https://dev.to/vinodchauhan7/react-hooks-with-async-await-1n9g)
* [useReducer Hook](https://reactjs.org/docs/hooks-reference.html#usereducer)
* [react custom hooks](https://reactjs.org/docs/hooks-custom.html)
* [use hooks](https://usehooks.com/)
* [hooks list](https://github.com/rehooks/awesome-react-hooks)
* [10 essential react hooks](https://blog.bitsrc.io/10-react-custom-hooks-you-should-have-in-your-toolbox-aa27d3f5564d)
* []

