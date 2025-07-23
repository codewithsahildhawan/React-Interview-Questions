# How to rerender a component on value change in React?

## Explanation
A React component automatically rerenders when its state or props change. Use the `useState` hook to manage state and trigger rerenders.

## Syntax
```jsx
const [value, setValue] = useState('');
// ...
setValue(newValue); // triggers rerender
```

## Example
```jsx
import React, { useState } from 'react';

function RerenderExample() {
  const [count, setCount] = useState(0);
  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={() => setCount(c => c + 1)}>Increment</button>
    </div>
  );
}
``` 