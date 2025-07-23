# Virtual DOM

## Explanation
The virtual DOM is a lightweight copy of the real DOM. React uses it to efficiently update the UI by comparing changes and updating only what is necessary.

## Syntax
```jsx
// No direct syntax, but React uses virtual DOM internally
```

## Example
```jsx
import React, { useState } from 'react';

function Counter() {
  const [count, setCount] = useState(0);
  return <button onClick={() => setCount(c => c + 1)}>Count: {count}</button>;
}
// React updates the virtual DOM and syncs with the real DOM
``` 