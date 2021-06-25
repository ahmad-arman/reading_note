### Why do we not need more .html pages in a multi-page React app?


React takes advantage of HTML’s popularity and strength as the most popular programming language, by letting you use a very similar syntax to HTML to build interfaces and add dynamic features to it using JavaScript.

#### If we wanted a component to show up on every page, where would we put it and why?
 * Outside the `<BrowserRouter/>`

* Inside the `<BrowserRouter />`, outside a `<Route />`
* Inside a `<Route />`
We put it inside the `<Route>`


#### What does props.children contain?

All the elements, values of the component, it’s useful if we need to render multiple components dynamically depending on the data needed to be rendered.



## Term 

* Composition :  React Composition is a development pattern based on React's original component model where we build components from other components using explicit defined props or the implicit children prop
* Children / Child Components : Children allow you to pass components as data to other components, just like any other prop you use. ... The special thing about children is that React provides support through its ReactElement API and JSX. XML children translate perfectly to React children!
* Hash Routing :  It uses URL hash, it puts no limitations on supported browsers or web server. Server-side routing is independent from client-side routing. Backward-compatible single-page application can use it as example.com/#/react/route.
* Link Routing : To add the link in the menu, use the `<NavLink />` component by react-router-dom . The NavLink component provides a declarative way to navigate around the application. It is similar to the Link component, except it can apply an active style to the link if it is active.



## Making Sense of React Hooks

Do Hooks Make React Bloated? <br>
If the React community embraces the Hooks proposal, it will reduce the number of concepts you need to juggle when writing React applications. Hooks let you always use functions instead of having to constantly switch between functions, classes, higher-order components, and render props.

* What Are Hooks, Exactly?
To understand Hooks, we need to take a step back and think about code reuse.
Today, there are a lot of ways to reuse logic in React apps. We can write simple functions and call them to calculate something. We can also write components (which themselves could be functions or classes). Components are more powerful, but they have to render some UI. This makes them inconvenient for sharing non-visual logic. This is how we end up with complex patterns like render props and higher-order components.


#### What is a Hook?
 A Hook is a special function that lets you “hook into” React features. For example, useState is a Hook that lets you add React state to function components. We’ll learn other Hooks later.

When would I use a Hook? If you write a function component and realize you need to add some state to it, previously you had to convert it to a class. Now you can use a Hook inside the existing function component. We’re going to do that right now!


#### What does calling useState do?
 It declares a “state variable”. Our variable is called count but we could call it anything else, like banana. This is a way to “preserve” some values between the function calls — useState is a new way to use the exact same capabilities that this.state provides in a class. Normally, variables “disappear” when the function exits but state variables are preserved by React.

### What do we pass to useState as an argument? 
The only argument to the `useState()` Hook is the initial state. Unlike with classes, the state doesn’t have to be an object. We can keep a number or a string if that’s all we need. In our example, we just want a number for how many times the user clicked, so pass 0 as initial state for our variable. (If we wanted to store two different values in state, we would call `useState()` twice.)

#### What does useState return?
 It returns a pair of values: the current state and a function that updates it. This is why we write const [count, setCount] = `useState()`. This is similar to this.state.count and this.setState in a class, except you get them in a pair. If you’re not familiar with the syntax we used, we’ll come back to it at the bottom of this page.


#### State Hook

```
import React, { useState } from 'react';

function Example() {
  // Declare a new state variable, which we'll call "count"
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>
        Click me
      </button>
    </div>
  );
}
```



Here, `useState` is a Hook (we’ll talk about what this means in a moment). We call it inside a function component to add some local state to it. React will preserve this state between re-renders. `useState` returns a pair: the current state value and a function that lets you update it. You can call this function from an event handler or somewhere else. It’s similar to `this.setState` in a class, except it doesn’t merge the old and new state together. (We’ll show an example comparing `useState` to` this.state` in Using the State Hook.)

The only argument to `useState` is the initial state. In the example above, it is 0 because our counter starts from zero. Note that unlike this.state, the state here doesn’t have to be an object — although it can be if you want. The initial state argument is only used during the first render.



#### Effect Hook 

You’ve likely performed data fetching, subscriptions, or manually changing the DOM from React components before. We call these operations “side effects” (or “effects” for short) because they can affect other components and can’t be done during rendering.

The Effect Hook, `useEffect`, adds the ability to perform side effects from a function component. It serves the same purpose as `componentDidMount`, `componentDidUpdate`, and `componentWillUnmount` in React classes, but unified into a single API. (We’ll show examples comparing `useEffect` to these methods in Using the Effect Hook.)

For example, this component sets the document title after React updates the DOM:

```
import React, { useState, useEffect } from 'react';

function Example() {
  const [count, setCount] = useState(0);

  // Similar to componentDidMount and componentDidUpdate:
  useEffect(() => {
    // Update the document title using the browser API
    document.title = `You clicked ${count} times`;
  });

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>
        Click me
      </button>
    </div>
  );
}
```















## REFERENCE 

* [making sense of hooks](https://medium.com/@dan_abramov/making-sense-of-react-hooks-fdbde8803889)
* [the state hook](https://reactjs.org/docs/hooks-state.html)
* [hooks api](https://reactjs.org/docs/hooks-overview.html)
* [hooks api reference](https://reactjs.org/docs/hooks-reference.html)
* [effects hook](https://reactjs.org/docs/hooks-effect.html)




