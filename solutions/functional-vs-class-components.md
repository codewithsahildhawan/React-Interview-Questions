# Functional vs Class components

## Explanation
Functional components are JavaScript functions that return JSX. Class components are ES6 classes that extend `React.Component` and have lifecycle methods and state.

## Syntax
```jsx
// Functional
function MyComponent() { return <div>Hello</div>; }
// Class
class MyComponent extends React.Component { render() { return <div>Hello</div>; } }
```

## Example
```jsx
import React from 'react';

// Functional
function Greet() { return <h1>Hello!</h1>; }

// Class
class Welcome extends React.Component {
  render() { return <h1>Welcome!</h1>; }
} 