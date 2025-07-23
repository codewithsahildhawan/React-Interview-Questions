# How to call parent component method from child component in React?

## Explanation
To call a parent component's method from a child component, pass the parent's method as a prop to the child. The child can then invoke this function prop.

## Syntax
```jsx
// Parent Component
<ChildComponent onAction={parentMethod} />

// Child Component
function ChildComponent({ onAction }) {
  return <button onClick={onAction}>Call Parent Method</button>;
}
```

## Example
```jsx
import React from 'react';

function Child({ onNotify }) {
  return <button onClick={onNotify}>Notify Parent</button>;
}

function Parent() {
  const handleNotify = () => alert('Called from child!');
  return <Child onNotify={handleNotify} />;
}
``` 