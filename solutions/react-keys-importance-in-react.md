# What are React keys and why are they important?

## Explanation
Keys help React identify which items have changed, are added, or are removed in a list. They should be unique and stable for each list item.

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