

### Does a deployed React application require a server? 
no 
### Why do we prefer to test a React application at the behavior rather than the unit level?
When it comes to React components you want to check how your component is rendered and if all props you pass to the component influence the behavior of your component as expected.
### What does npm run build do?
runs the build field from the package.json scripts field <br>
 creates a build directory with a production build of your app.
### Describe the actual composition / architecture of a React application

React application is split into components, it is important that you can add functionality to a component without causing rippling changes through the codebase


## Terms 

1- BDD :Behavior driven development, a branch of Test Driven Development (TDD), which uses human-readable descriptions of software user requirements as the basis for software tests.

2- mounting : is the phase in which our React component mounts on the DOM (i.e., is created and inserted into the DOM). This method is called just before a component mounts on the DOM or the render method is called. After this method, the component gets mounted

3-Acceptance Tests: Acceptance testing is a term used in agile software development methodologies, particularly extreme programming, referring to the functional testing of a user story by the software development team during the implementation phase.

4-build: React apps are built. Writing a react app is called building.


## Preparation Materials

 * setState 

 1-) setState React components with state render UI based on that state. When the state of components changes, so does the component UI. setState() is the only way to update state after the initial state setup.
 2 -) Update to a component state should be done using setState() also you can pass an object or a function to setState() .

 * State 
  
   The state is an instance of React Component Class can be defined as an object of a set of observable properties that control the behavior of the component. In other words, the State of a component is an object that holds some information that may change over the lifetime of the component.

 * Props  
    is a special keyword in React, which stands for properties and is being used for passing data from one component to another. Furthermore, props data is read-only, which means that data coming from the parent should not be changed by child components.
    
 *   Handling forms is about how you handle the data when it changes value or gets submitted. In HTML, form data is usually handled by the DOM. In React, form data is usually handled by the components.  When the data is handled by the components, all the data is stored in the component state

 
