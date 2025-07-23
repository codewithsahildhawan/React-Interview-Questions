# Explain React's reconciliation process

## Explanation
Reconciliation is the process React uses to update the DOM by comparing the new virtual DOM with the previous one and applying only the necessary changes.

## Syntax
```jsx
// No direct syntax, handled internally by React
```

## Example
```jsx
import React, { useState } from 'react';

function List() {
  const [items, setItems] = useState(['A', 'B', 'C']);
  return (
    <ul>
      {items.map(item => <li key={item}>{item}</li>)}
    </ul>
  );
}
// React efficiently updates only changed list items
``` 