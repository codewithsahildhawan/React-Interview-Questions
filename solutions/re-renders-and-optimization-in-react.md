# Re-renders & optimization

## Explanation
Re-renders occur when state or props change. Optimization techniques include memoization, virtualization, and avoiding unnecessary state updates.

## Syntax
```jsx
const Memoized = React.memo(Component);
const memoValue = useMemo(() => compute(), [deps]);
```

## Example
```jsx
import React, { useMemo, useState } from 'react';

function Expensive({ num }) {
  const value = useMemo(() => {
    let total = 0;
    for (let i = 0; i < 1e7; i++) total += num;
    return total;
  }, [num]);
  return <div>{value}</div>;
}
``` 