# How do you send data from parent component to child component in React?

## Explanation
In React, data is sent from a parent component to a child component via props. The parent passes data as attributes to the child component.

## Syntax
```jsx
// Parent Component
<ChildComponent someProp={value} />

// Child Component
function ChildComponent(props) {
  return <div>{props.someProp}</div>;
}
```

## Example
```jsx
import React from 'react';

function Child({ message }) {
  return <h2>{message}</h2>;
}

function Parent() {
  return <Child message="Hello from Parent!" />;
}
``` 