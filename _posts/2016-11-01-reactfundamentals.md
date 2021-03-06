---
layout: post
title: "React JS"
image: "http://mjw56.github.io/content/images/2015/05/react_native.png"
categories:
  - Learning
  - Projects
  - Courses
tags:
  - Javascript
  - React
  - Redux
  - Fundamentals
---
# React: The Right Way
---

**Architecture**

A React application is composed by a set of components. The inputs to components properties and referred to as **props** or **state**.  

State is different from props because it can change. It is best to design around components that don't use state. Props and state collectively represent the **model**. The **Document Object Model** is rendered from this model.  

You can change the DOM by changing the model. **Events** can trigger state changes. These state changes sparks another render loop. React sustains a fake DOM abstraction. The changes are then updated to the real DOM is the most efficient way possible.  

* React & Knockout JS
  * Both provide:
   * Rendering to DOM
   * Events
* React & Angular & Ember
  * Larger and more generalized
* React & Backbone
    * Common to use React as alternate view for Backbone

**Components**

Each component corresponds to an element in the DOM. Components can be **nested**. Same interaction for the DOM elements.  

Top level namespace is React. Minimum requirement is a render function.

| Aspects | Description |
| --- |: --- |
| JSX | Allows us to write HTML like syntax which gets transformed to lightweight JavaScript objects.  |
| Virtual DOM | A JavaScript representation of the actual DOM.  |
| React.createClass | The way in which you create a new component.  |
| render (method) | What we would like our HTML Template to look like.  
| ReactDOM.render | Renders a React component to a DOM node.  
| state | The internal data store (object) of a component.  
| getInitialState | The way in which you set the initial state of a component.  
| setState | A helper method for altering the state of a component.  
| props | The data which is passed to the child component from the parent component.  
| propTypes | Allows you to control the presence, or types of certain props passed to the child  component.  |
| getDefaultProps | Allows you to set default props for your component. |

| Component LifeCycle  |
| :--- |
| componentWillMount — Fired before the component will mount |
| componentDidMount — Fired after the component mounted  |
| componentWillReceiveProps — Fired whenever there is a change to props |  
| componentWillUnmount — Fired before the component will unmount |
| Events  |
| onClick  |
| onSubmit  |
| onChange  |  

# Overview  

* Project Setup
* JSX/Babel
* Component States
* Component Props
* Working with Forms  

Installations:  
1. Go ahead and install [nodeJS](nodejs.org)  
2. Go to nodeJS command prompt
3. npm install -g webpack gulp
4. cd /directoryOfReactProject/
5. npm install (uses package.json)
6. gulp
7. gulp server (new windows)
8. localhost:8080

**Project Tools**  

| Name | Purpose |
| :--- | :--- |
| Node.Js | Serverside Javascript powered by Google's V8 Javascript Engine |
| Gulp | Javascript task runner for pre-processing source code and webserver |
| SASS | Transpile SASS source files to CSS |
| Babel | Transpile JSX and ECMAScript 2015 source files to ES5.1 Javascript |
| WebPack | Provides module and packaging system for working with Javascript files |
| Express | Configuring web server and Node.Js HTTP module to serve web app |
| Visual Studio Code | Text editor |

npm install creates the node modules folder  
gulp creates the dist folder for serving to web hosting
Two React Javascript files are needed for web application usage (one for react, one for web browser DOM)  
Define component
Instantiate the component  
Place into DOM  

**React Component Props**  
Props are immutable parameters of the component. They are passed in by the parent component and then React then updates by comparing the current DOM with old props and the new DOM with new props.  

This uses a virtual DOM and is called reconciliation.
We use this to refer to the component and props to the parameters handed in.

**React Component States**  
On the flip side, here are our mutable parameters. the function setState will trigger React to re-render the component with new state values. Ideally very few components should have state. The parent should manage the state and then pass that down to the children with props. This is the common practice to have child receive props triggered by state.  

**React Forms**  
React forms are different from other UI libraries. The state of the component must be synced with the DOM, this makes typing into inputs challenging. This is because every keystroke does not actually update the value attribute. React hooks onto the onChance function to rerender the DOM on every key press. Form controls which are not managed with onChange are considered uncontrolled forms.  
