### Why choose Redux instead of the Context API for global state?

Context API is easy to is use as it has a short learning curve. It requires less code, and because there's no need of extra libraries, bundle sizes are reduced. Redux on the other hand requires adding more libraries to the application bundle. The syntax is complex and extensive creating unnecessary work and complexity.

### What is the purpose of a reducer?

A reducer is a function that determines changes to an application's state. It uses the action it receives to determine this change. We have tools, like Redux, that help manage an application's state changes in a single store so that they behave consistently.

### What does an action contain?

Actions have a type field that tells what kind of action to perform and all other fields contain information or data. And there is one other term called Action Creators, these are the function that creates actions. So actions are the information (Objects) and action creator are functions that return these actions.



### Why do we need to copy the state in a reducer?

In the documentation of reducers(read it again for details!), redux only requires our reducers to stay pure. If the new state is different, the reducer must create new object, and making a copy is a way to describe the unchanged part



### Term 

* immutable state : Redux is a small library that represents state as (immutable) objects. And new states by passing the current state through pure functions to create an entirely new object/application states. ... They never mutate, returning newly built objects: This allows reasoning about input + output without side-effects. <br>

* time travel in redux :  Time travel is the ability to move back and forth among the previous states of an application and view the results in real time. With Redux, given a specific state and a specific action, the next state of the application is always exactly the same <br>

* action creator :  is a function that literally creates an action object. In Redux, action creators simply return an action object and pass the argument value if necessary. <br>

* reducer :  is a function that determines changes to an application's state. It uses the action it receives to determine this change. We have tools, like Redux, that help manage an application's state changes in a single store so that they behave consistently. <br>

* dispatch : s the method used to dispatch actions and trigger state changes to the store. react-redux is simply trying to give you convenient access to it. Note, however, that dispatch is not available on props if you do pass in actions to your connect function. <br>




#### Core Concepts 

 The most common state shape for a Redux app is a plain Javascript object containing "slices" of domain-specific data at each top-level key. Similarly, the most common approach to writing reducer logic for that state shape is to have "slice reducer" functions, each with the same (state, action) signature, and each responsible for managing all updates to that specific slice of state. Multiple slice reducers can respond to the same action, independently update their own slice as needed, and the updated slices are combined into the new state object.

Because this pattern is so common, Redux provides the combineReducers utility to implement that behavior. It is an example of a higher-order reducer, which takes an object full of slice reducer functions, and returns a new reducer function.

1- First and foremost, combineReducers is simply a utility function to simplify the most common use case when writing Redux reducers. You are not required to use it in your own application, and it does not handle every possible scenario. It is entirely possible to write reducer logic without using it, and it is quite common to need to write custom reducer logic for cases that combineReducer does not handle. (See Beyond combineReducers for examples and suggestions.)

2-While Redux itself is not opinionated about how your state is organized, combineReducers enforces several rules to help users avoid common errors. (See combineReducers for details.)

3-One frequently asked question is whether Redux "calls all reducers" when dispatching an action. Since there really is only one root reducer function, the default answer is "no, it does not". However, combineReducers has specific behavior that does work that way. In order to assemble the new state tree, combineReducers will call each slice reducer with its current slice of state and the current action, giving the slice reducer a chance to respond and update its slice of state if needed. So, in that sense, using combineReducers does "call all reducers", or at least all of the slice reducers it is wrapping.

4- You can use it at all levels of your reducer structure, not just to create the root reducer. It's very common to have multiple combined reducers in various places, which are composed together to create the root reducer.

#### Defining State Shape 

There are two ways to define the initial shape and contents of your store's state. First, the createStore function can take preloadedState as its second argument. This is primarily intended for initializing the store with state that was previously persisted elsewhere, such as the browser's localStorage. The other way is for the root reducer to return the initial state value when the state argument is undefined. These two approaches are described in more detail in Initializing State, but there are some additional concerns to be aware of when using combineReducers.

combineReducers takes an object full of slice reducer functions, and creates a function that outputs a corresponding state object with the same keys. This means that if no preloaded state is provided to createStore, the naming of the keys in the input slice reducer object will define the naming of the keys in the output state object. The correlation between these names is not always apparent, especially when using ES6 features such as default module exports and object literal shorthands.


```
// reducers.js
export default theDefaultReducer = (state = 0, action) => state

export const firstNamedReducer = (state = 1, action) => state

export const secondNamedReducer = (state = 2, action) => state

// rootReducer.js
import { combineReducers, createStore } from 'redux'

import theDefaultReducer, {
  firstNamedReducer,
  secondNamedReducer
} from './reducers'

// Use ES6 object literal shorthand syntax to define the object shape
const rootReducer = combineReducers({
  theDefaultReducer,
  firstNamedReducer,
  secondNamedReducer
})

const store = createStore(rootReducer)
console.log(store.getState())
// {theDefaultReducer : 0, firstNamedReducer : 1, secondNamedReducer : 2}
```

### combineReducers(reducers)

As your app grows more complex, you'll want to split your reducing function into separate functions, each managing independent parts of the state.

The combineReducers helper function turns an object whose values are different reducing functions into a single reducing function you can pass to createStore.

The resulting reducer calls every child reducer, and gathers their results into a single state object. The state produced by combineReducers() namespaces the states of each reducer under their keys as passed to combineReducers()

```
rootReducer = combineReducers({potato: potatoReducer, tomato: tomatoReducer})
// This would produce the following state object
{
  potato: {
    // ... potatoes, and other state managed by the potatoReducer ...
  },
  tomato: {
    // ... tomatoes, and other state managed by the tomatoReducer, maybe some nice sauce? ...
  }
}
```

You can control state key names by using different keys for the reducers in the passed object. For example, you may call combineReducers({ todos: myTodosReducer, counter: myCounterReducer }) for the state shape to be { todos, counter }.

A popular convention is to name reducers after the state slices they manage, so you can use ES6 property shorthand notation: combineReducers({ counter, todos }). This is equivalent to writing combineReducers({ counter: counter, todos: todos }).


### REFERENCE 




* [Multiple Reducers Example](https://www.youtube.com/watch?v=gBER4Or86hE)
* [Redux Docs: Using Combined Reducers](https://redux.js.org/usage/structuring-reducers/using-combinereducers/)
* [Redux Docs: Combined Reducer Syntax](https://redux.js.org/api/combinereducers/)
