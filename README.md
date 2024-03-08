# LearningReact
This is a repository for learning React.js , React create SPA (Single Page Application) and React is a library for building user interfaces.



## Day 1 4/3/2024

### Code to create vite project and normal react project
```jsx
//vite project
npx create vite@latest 
//normal react project
npx create-react-app my-react-project
```

### What is vite and parcel

Vite is a bundler (bhaur sare file me js likhte hai usko ekk file me convert karta hai)

### What is React
React is a library for building user interfaces
![alt text](image-1.png) (React-dom for web and React-native for mobile app)

TO build a react project :

## Day 2 5-03-2024

### What is differnce in JS and JSX and why it is necessary to name component file in vite .jsx extension.

Jsx is a syntax extension for javascript. It is used with React componenets. It is not necessary to use .jsx extension for vite file but it is recommended to use it.

### some convetions in vite

1. first letter should be captial in component name
2. while importing a component, it should be also first letter captial
ex
import Chai from './Chai.jsx';
3. component name should be name with jsx extension

### Frangments in react
Fragments let you group a list of children without adding extra nodes to the DOM.
//frangments syntax
```jsx  
<>
  <h1>hello</h1>
  <h2>world</h2>
</>
```

### React kya krta hai ekk root create krta hai aur uske andar sare component ko render krta hai
, basically wo <App/> component ko render krta hai jo ki ekk js or jsx file hota hai jisme ekk function hota hai jo ki html ko export krta hai.


### Object literals.

there are two ways to create object in javascript
1. using object literal syntax
2. using object constructor syntax

```jsx
//object literal syntax
let person = {
  name: 'john',
  age: 30
}

//object constructor syntax
let person = new Object();
person.name = 'john';
person.age = 30;
```
second method is not recommended because it is slow and singelton object is created in this method. (singelton object is a object which is created only once and used everywhere in the code) 

### variables in javascript
 A variable can appear to be used before it's declared. This behavior is called hoisting, as it appears that the variable declaration is moved to the top of the function, static initialization block, or script source in which it occurs.
 
### React createElement syntax and example ans order of parameters
```jsx
//syntax
React.createElement('h1', {className: 'greeting'}, 'Hello, world!');
//example
React.createElement('h1', {className: 'greeting'}, 'Hello, world!');
```
order of parameters
1. type
2. props or null 
3. children (ie. text or other elements)

### How to pass js in jsx
```jsx
//syntax
const name = 'Josh Perez';
const element = <h1>Hello, {name}</h1>;
```
{} is used to pass js in jsx
called evaluated expression which is evaluated and then passed to jsx so you can't use directly if else or for loop in it.

### Babel and JSX

We use Babel with React to transpile (ie converts source code from a programming language into an equivalent source code of the same or a different programming language.  ) the JSX code into simple React functions that can be understood by browsers. Babel is a JavaScript compiler that can convert markup language into JavaScript. 



## Day 3 6-03-2024

### Hooks in react
Hooks are used to sync the variable state with the UI. It is used to update the state of the varible everywere it is used in the code.

syntax of hooks
```jsx  
import React, { useState } from 'react';
function Example() {
  // Declare a new state variable, which we'll call "count"
  const [count, setCount] = useState(0); //here count is the variable and setCount is the function to update the state of the variable count and 0 is the initial value of the variable count 
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
useState is a hook which is used to update the state of the variable. It is used to update the state of the variable everywere it is used in the code.


## Day 4 7-03-2024

### Vertual dom 

The virtual DOM (VDOM) is a programming concept where an ideal, or “virtual”, representation of a UI is kept in memory and synced with the “real” DOM by a library such as ReactDOM. This process is called reconciliation.
and mapping of the real dom is done with the virtual dom and replacing the only those elements which are in vitual dom and not in real dom.

### reconciliation

Reconciliation is the process through which React updates the DOM. When a component’s state changes, React has to update the component’s rendered view. This process is called reconciliation.  

### What is rendering in react

Rendering is the process of updating the DOM with the correct user interface. React components are used to render the view of the application. When the state of a component changes, React has to determine what changes need to be made to the view and update the DOM to reflect those changes.

### What is createRoot in react and how it is related to virtual dom and rendering in react   

createRoot is used to create a root for the virtual dom and it is used to render the virtual dom to the real dom. 


## Day 5 8-03-2024

### Tailwind CSS and how to install it in vite project

See Tailwind website for installation of tailwind in vite project

### What is props and how to pass props in react

Props are used to pass the data from HTML tag in main.jsx to the component (ex app.jsx or customMade.jsx). 

Example : 
```jsx
//main.jsx
import React from 'react';
import ReactDOM from 'react-dom';
import App from './App.jsx';
ReactDOM.render(
  <App name="Chai"/>
);

//App.jsx
import React from 'react';
function App(props) {
  return (
    <div>
      <h1>Hello, {props.name}</h1>
    </div>
  );
}


```
In this example, name is passed from main.jsx to App.jsx using props.





















