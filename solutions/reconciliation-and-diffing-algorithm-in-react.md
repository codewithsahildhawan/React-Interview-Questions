# Reconciliation & diffing algorithm

## Explanation
React's reconciliation algorithm compares the new virtual DOM with the previous one and updates only the changed parts in the real DOM.

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