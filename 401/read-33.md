#### What’s the best practice for “pre-loading” data into the store (on application start) in a Redux application?

 The most 'redux-like' way of handling the pre-loading of data would be to fire off the asynchronous action in the lifecycle method (probably componentWillMount ) of a Higher Order Component that wraps your app

#### When using a thunk/async action that dispatches the actual action, which do you export from your reducer?

Thunk is for communicating asynchronously with an external API to retrieve or save data. Redux Thunk makes it easy to dispatch actions that follow the lifecycle of a request to an external API


##  Term

* thunk :  middleware that allows you to return functions, rather than just actions, within Redux. This allows for delayed actions, including working with promises. One of the main use cases for this middleware is for handling actions that might not be synchronous, for example, using axios to send a GET request <br>

* middleware : provides a third-party extension point between dispatching an action, and the moment it reaches the reducer. People use Redux middleware for logging, crash reporting, talking to an asynchronous API,


### Redux Toolkit Quick Starts


 Since Redux Toolkit is an abstraction layer that wraps around the Redux core, it's helpful to know what RTK's APIs are actually doing for you under the hood. If you want to understand how Redux really works and why RTK is the recommended approach, read the Redux Fundamentals tutorial.

#### Redux Essentials: A Real-World Example#
The Redux Essentials tutorial teaches you "how to use Redux the right way", using Redux Toolkit as the standard approach for writing Redux logic.

It shows how to build a "real world"-style example application, and teaches Redux concepts along the way.

If you've never used Redux before, and just want to know "how do I use this to build something useful?", start with the Redux Essentials tutorial.


#### Redux Fundamentals: Redux from the Ground Up#
The Redux Fundamentals tutorial teaches "how Redux works, from the bottom up", by showing how to write Redux code by hand and why standard usage patterns exist. It then shows how Redux Toolkit simplifies those Redux usage patterns.

Since Redux Toolkit is an abstraction layer that wraps around the Redux core, it's helpful to know what RTK's APIs are actually doing for you under the hood. If you want to understand how Redux really works and why RTK is the recommended approach, read the Redux Fundamentals tutorial.

### Using Redux Toolkit
The RTK Usage Guide docs page explains the standard usage patterns for each of RTK's APIs. The API Reference section describes each API function and has additional usage examples.

The Redux Essentials tutorial also shows how to use each of the APIs while building an application.

### Migrating Vanilla Redux to Redux Toolkit
If you already know Redux and just want to know how to migrate an existing application to use Redux Toolkit, the "Modern Redux with Redux Toolkit" page in the Redux Fundamentals tutorial shows how RTK's APIs simplify Redux usage patterns and how to handle that migration

#### Using Redux Toolkit with TypeScript
The RTK docs page on Usage with TypeScript shows the basic pattern for setting up Redux Toolkit with TypeScript and React, and documents specific TS patterns for each of the RTK APIs.

In addition, the Redux + TS template for Create-React-App comes with RTK already configured to use those TS patterns, and serves as a good example of how this should work

#### Legacy Redux Toolkit Tutorials
We previously had a set of "Basic/Intermediate/Advanced" tutorials directly in the Redux Toolkit docs. They were helpful, but we've removed them in favor of pointing to the "Essentials" and "Fundamentals" tutorials in the Redux core docs.



### MobX 
MobX is a simple, scalable and battle tested state management solution. This tutorial will teach you all the important concepts of MobX in ten minutes. MobX is a standalone library, but most people are using it with React and this tutorial focuses on that combination.

#### The core idea
State is the heart of each application and there is no quicker way to create buggy, unmanageable applications than by producing an inconsistent state or state that is out-of-sync with local variables that linger around. Hence many state management solutions try to restrict the ways in which you can modify state, for example by making state immutable. But this introduces new problems; data needs to be normalized, referential integrity can no longer be guaranteed and it becomes next to impossible to use powerful concepts like classes in case you fancy those.


#### REFERENCE 

* [Redux Toolkit (RTK)](https://redux-toolkit.js.org/)
* [Tutorial](https://redux-toolkit.js.org/tutorials/overview)

* [MobX](https://mobx.js.org/getting-started.html)

* [HookState](https://hookstate.js.org/)


