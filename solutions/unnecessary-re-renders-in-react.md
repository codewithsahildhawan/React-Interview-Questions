# What causes unnecessary re-renders in React?

## Explanation
Unnecessary re-renders occur when a component re-renders without any meaningful change. Causes include changing state/props unnecessarily, new object/function references, or context updates.

## Syntax
```jsx
// Avoid creating new objects/functions in render
const memoized = useMemo(() => value, [value]);
const callback = useCallback(() => fn(), [deps]);
```

## Example
```jsx
import React, { useState, useCallback } from 'react';

function Parent() {
  const [count, setCount] = useState(0);
  const handleClick = useCallback(() => setCount(c => c + 1), []);
  return <Child onClick={handleClick} />;
}

const Child = React.memo(({ onClick }) => {
  return <button onClick={onClick}>Click</button>;
});
``` 