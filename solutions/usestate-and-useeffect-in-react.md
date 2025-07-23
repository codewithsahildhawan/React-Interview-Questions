# useState & useEffect

## Explanation
`useState` is a hook for managing state in functional components. `useEffect` is a hook for running side effects (like data fetching or subscriptions).

## Syntax
```jsx
const [state, setState] = useState(initialValue);
useEffect(() => { /* effect */ }, [deps]);
```

## Example
```jsx
import React, { useState, useEffect } from 'react';

function Example() {
  const [count, setCount] = useState(0);
  useEffect(() => {
    document.title = `Count: ${count}`;
  }, [count]);
  return <button onClick={() => setCount(c => c + 1)}>Increment</button>;
} 