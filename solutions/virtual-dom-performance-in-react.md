# How does React's Virtual DOM improve performance?

## Explanation
The virtual DOM allows React to batch and minimize real DOM updates by comparing virtual trees and applying only the necessary changes.

## Syntax
```jsx
// No direct syntax, handled internally by React
```

## Example
```jsx
import React, { useState } from 'react';

function Counter() {
  const [count, setCount] = useState(0);
  return <button onClick={() => setCount(c => c + 1)}>Count: {count}</button>;
}
// React updates the virtual DOM and syncs with the real DOM efficiently
``` 