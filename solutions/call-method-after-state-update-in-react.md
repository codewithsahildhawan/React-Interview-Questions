# How to call a method immediately after state is updated or after component is rerendered?

## Explanation
Use the `useEffect` hook and add the state variable as a dependency. The effect runs after the state updates and the component rerenders.

## Syntax
```jsx
useEffect(() => {
  // code to run after state update
}, [stateVar]);
```

## Example
```jsx
import React, { useState, useEffect } from 'react';

function AfterUpdate() {
  const [count, setCount] = useState(0);
  useEffect(() => {
    if (count > 0) alert('Count updated!');
  }, [count]);
  return (
    <button onClick={() => setCount(c => c + 1)}>Increment</button>
  );
}
``` 