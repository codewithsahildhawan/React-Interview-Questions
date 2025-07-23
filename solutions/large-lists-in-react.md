# How to handle large lists efficiently?

## Explanation
For large lists, use virtualization libraries like `react-window` or `react-virtualized` to render only visible items and improve performance.

## Syntax
```jsx
import { FixedSizeList as List } from 'react-window';
<List height={400} itemCount={1000} itemSize={35} width={300}>
  {Row}
</List>
```

## Example
```jsx
import React from 'react';
import { FixedSizeList as List } from 'react-window';

const Row = ({ index, style }) => (
  <div style={style}>Row {index}</div>
);

function VirtualizedList() {
  return (
    <List height={150} itemCount={1000} itemSize={30} width={300}>
      {Row}
    </List>
  );
}
``` 