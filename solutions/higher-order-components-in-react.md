# Higher-Order Components (HOCs)

## Explanation
A higher-order component is a function that takes a component and returns a new component with enhanced behavior.

## Syntax
```jsx
function withFeature(Component) {
  return function Enhanced(props) {
    // ...
    return <Component {...props} />;
  };
}
```

## Example
```jsx
import React from 'react';

function withLogger(Wrapped) {
  return function Logger(props) {
    console.log('Props:', props);
    return <Wrapped {...props} />;
  };
}

function Hello({ name }) {
  return <h1>Hello, {name}</h1>;
}

const HelloWithLogger = withLogger(Hello);
``` 