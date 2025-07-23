# Give an example of optimization using useCallback in React.

## Explanation
The `useCallback` hook memoizes a function, preventing its recreation unless dependencies change. Useful for passing stable callbacks to child components.

## Syntax
```jsx
const memoizedCallback = useCallback(() => { /* ... */ }, [deps]);
```

## Example
```jsx
import React, { useState, useCallback } from 'react';

function Button({ onClick, children }) {
  return <button onClick={onClick}>{children}</button>;
}

function Counter() {
  const [count, setCount] = useState(0);
  const increment = useCallback(() => setCount(c => c + 1), []);
  return <Button onClick={increment}>Increment: {count}</Button>;
} 