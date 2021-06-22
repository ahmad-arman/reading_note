### Do child components have direct access to props/state from the parent?
NO ,
 To be able to access and update state from the child component, we can add a method that handles updating the state to the parent component and pass the method as a prop to the child component instead of the state itself
### When a component “wraps” another component, how does the child component’s output get rendered?
 components that surround unknown components and provide a default structure to display the child components. This pattern is useful for creating user interface (UI) elements that are used repeatedly throughout a design, like modals, template pages, and information tiles.

### Can a component, such as Content, which is a child also be used as a standalone component elsewhere in the application? 
yes 

### What trick can a parent use to share all props with it’s children


Using Inheretence.



##  Term

* props.children :that it is used to display whatever you include between the opening and closing tags when invoking a component.

* composition :  is a development pattern based on React's original component model where we build components from other components using explicit defined props or the implicit children prop


## A Simple React Router v4 Tutorial

React Router v4 is a pure React rewrite of the popular React package. Previous versions of React Router used configuration disguised as pseudo-components and could be difficult to understand. With v4, everything is “just components”

 * Single-page application? A single-page application (SPA) is a website that re-renders its content in response to navigation actions (e.g. clicking a link) without making a request to the server to fetch new HTML.

 * Installation
React Router has been broken into three packages: <br>
`react-router`, `react-router-dom`, and `react-router-native`.

You should almost never have to install `react-router` directly. That package provides the core routing components and functions for React Router applications. The other two provide environment specific (browser and React Native) components, but they both also re-export all of react-router's exports.

We are building a website (something that will be run in browsers), so we will install `react-router-dom`.

`npm install --save react-router-dom`

* Rendering a `<Router>`
Router components only expect to receive a single child element. To work within this limitation, it is useful to create an `<App>` component that renders the rest of your application. Separating your application from the router is also useful for server rendering because you can re-use the `<App> `on the server while switching the router to a `<MemoryRouter>`.

* Path
A <`Route>` expects a path prop, which is a string that describes the pathname that the route matches — for example, `<Route path='/roster'/>` should match a pathname that begins with /roster 2. When the current location’s pathname is matched by the path, the route will render a React element. When the path does not match, the route will not render anything 


```
<Route path='/roster'/>
// when the pathname is '/', the path does not match
// when the pathname is '/roster' or '/roster/2', the path matches
// If you only want to match '/roster', then you need to use
// the "exact" prop. The following will match '/roster', but not
// '/roster/2'.
<Route exact path='/roster'/>
// You might find yourself adding the exact prop to most routes.
// In the future (i.e. v5), the exact prop will likely be true by
// default. For more information on that, you can check out this
// GitHub issue:
// https://github.com/ReactTraining/react-router/issues/4958
```

* What does the `<Route> `render?
Routes have three props that can be used to define what should be rendered when the route’s path matches. Only one should be provided to a `<Route>` element.

   * component — A React component. When a route with a component prop matches, the route will return a new element whose type is the provided React component (created using React.createElement).

   * render — A function that returns a React element 5. It will be called when the path matches. This is similar to component, but is useful for inline rendering and passing extra props to the element.

   * children — A function that returns a React element. Unlike the prior two props, this will always be rendered, regardless of whether the route’s path matches the current location.

## REFERENCE 
* [browser router tutorial](https://blog.pshrmn.com/simple-react-router-v4-tutorial/)

* [browser router api docs](https://reactrouter.com/web/api)

* [react-if component](https://www.npmjs.com/package/react-if)

* [react testing library queries](https://testing-library.com/docs/queries/about/)

* [aria roles](https://www.w3.org/TR/html-aria/)