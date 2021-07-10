#### Compare and Contrast Redux Toolkit with Redux “Ducks”

Ducks is a modular pattern that collocates actions, action types and reducers.


#### What is the principle advantage of Redux Toolkit

makes it easier to write good Redux applications and speeds up development, by baking in our recommended best practices, providing good default behaviors, catching mistakes, and allowing you to write simpler code. Redux Toolkit is beneficial to all Redux users regardless of skill level or experience


## Term
* redux toolkit slices : A function that accepts an initial state, an object full of reducer functions, and a "slice name", and automatically generates action creators and action types that correspond to the reducers and state. This API is the standard approach for writing Redux logic. <br>
* namespace :  is a group of related elements that each have a unique name or identifier. ... A file path, which uses syntax defined by the operating system, is considered a namespace. For example, C:\Program Files\Internet Explorer is the namespace that describes where Internet Explorer files on a Windows computer.<br>


### React Native 
is like React, but it uses native components instead of web components as building blocks. So to understand the basic structure of a React Native app, you need to understand some of the basic React concepts, like JSX, components, state, and props. If you already know React, you still need to learn some React-Native-specific stuff, like the native components. This tutorial is aimed at all audiences, whether you have React experience or not.

*  Components : 
So this code is defining HelloWorldApp, a new Component. When you're building a React Native app, you'll be making new components a lot. Anything you see on the screen is some sort of component.

* Props
Most components can be customized when they are created, with different parameters. These creation parameters are called props.

Your own components can also use props. This lets you make a single component that is used in many different places in your app, with slightly different properties in each place. Refer to props.YOUR_PROP_NAME in your functional components or this.props.YOUR_PROP_NAME in your class components. Here's an example:

```
import React from 'react';
import { Text, View, StyleSheet } from 'react-native';

const styles = StyleSheet.create({
  center: {
    alignItems: 'center'
  }
})

const Greeting = (props) => {
  return (
    <View style={styles.center}>
      <Text>Hello {props.name}!</Text>
    </View>
  );
}

const LotsOfGreetings = () => {
  return (
    <View style={[styles.center, {top: 50}]}>
      <Greeting name='Rexxar' />
      <Greeting name='Jaina' />
      <Greeting name='Valeera' />
    </View>
  );
}

export default LotsOfGreetings;
```

#### State
Unlike props that are read-only and should not be modified, the state allows React components to change their output over time in response to user actions, network responses and anything else

 * What's the difference between state and props in React? 
In a React component, the props are the variables that we pass from a parent component to a child component. Similarly, the state are also variables, with the difference that they are not passed as parameters, but rather that the component initializes and manages them internally. 


### Create native apps for Android and iOS using React
React Native combines the best parts of native development with React, a best-in-class JavaScript library for building user interfaces.

### Use a little—or a lot.
 You can use React Native today in your existing Android and iOS projects or you can create a whole new app from scratch.

#### Native Development For Everyone
React Native lets you create truly native apps and doesn't compromise your users' experiences. It provides a core set of platform agnostic native components like View, Text, and Image that map directly to the platform’s native UI building blocks.

#### Seamless Cross-Platform
React components wrap existing native code and interact with native APIs via React’s declarative UI paradigm and JavaScript. This enables native app development for whole new teams of developers, and can let existing native teams work much faster.


#### REFERENCE 

* [getting started with react native](https://reactnative.dev/docs/getting-started)
* [react native basics (Tutorial)](https://reactnative.dev/docs/tutorial)
* [react native](https://reactnative.dev/)
* [expo](https://expo.io/)
* [expo snack](https://snack.expo.io/)
* [ejecting](https://docs.expo.io/expokit/eject/?redirected)







