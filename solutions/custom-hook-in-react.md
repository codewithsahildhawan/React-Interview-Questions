# Create a custom hook.

## Explanation
A custom hook is a reusable function that uses React hooks to encapsulate logic. It must start with `use`.

## Syntax
```jsx
function useCustomHook() {
  // logic
}
```

## Example
```jsx
import { useState } from 'react';

function useCounter(initial = 0) {
  const [count, setCount] = useState(initial);
  const increment = () => setCount(c => c + 1);
  return [count, increment];
}

function Counter() {
  const [count, increment] = useCounter();
  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={increment}>Increment</button>
    </div>
  );
}
``` 