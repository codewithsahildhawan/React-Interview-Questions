# How to call a method on every rerender of a component?

## Explanation
Use the `useEffect` hook without a dependency array to call a method on every render (initial and updates).

## Syntax
```jsx
useEffect(() => {
  // code to run on every render
});
```

## Example
```jsx
import React, { useState, useEffect } from 'react';

function EveryRender() {
  const [count, setCount] = useState(0);
  useEffect(() => {
    console.log('Component rendered!');
  });
  return (
    <div>
      <button onClick={() => setCount(c => c + 1)}>Rerender</button>
    </div>
  );
}
``` 