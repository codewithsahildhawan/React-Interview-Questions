# Create a counter component using useState?

## Explanation
You can create a counter by using the `useState` hook to store the count and updating it with button clicks.

## Syntax
```jsx
const [count, setCount] = useState(0);
<button onClick={() => setCount(count + 1)}>Increment</button>
```

## Example
```jsx
import React, { useState } from 'react';

function Counter() {
  const [count, setCount] = useState(0);
  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={() => setCount(c => c + 1)}>Increment</button>
      <button onClick={() => setCount(c => c - 1)}>Decrement</button>
    </div>
  );
}
``` 