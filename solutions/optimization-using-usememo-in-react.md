# Give an example of optimization using useMemo.

## Explanation
The `useMemo` hook memoizes the result of a computation, preventing expensive calculations on every render unless dependencies change.

## Syntax
```jsx
const memoizedValue = useMemo(() => computeExpensiveValue(a, b), [a, b]);
```

## Example
```jsx
import React, { useState, useMemo } from 'react';

function ExpensiveComponent({ num }) {
  const expensive = useMemo(() => {
    let total = 0;
    for (let i = 0; i < 1e7; i++) total += num;
    return total;
  }, [num]);
  return <div>Expensive value: {expensive}</div>;
}
``` 