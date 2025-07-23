# Key prop in lists

## Explanation
The `key` prop helps React identify which items have changed, are added, or are removed in a list. Keys should be unique and stable.

## Syntax
```jsx
{items.map(item => <li key={item.id}>{item.value}</li>)}
```

## Example
```jsx
import React from 'react';

const items = [
  { id: 1, value: 'A' },
  { id: 2, value: 'B' }
];

function List() {
  return (
    <ul>
      {items.map(item => <li key={item.id}>{item.value}</li>)}
    </ul>
  );
}
``` 