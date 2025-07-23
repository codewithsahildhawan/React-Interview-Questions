# Explain useMemo() and useCallback() hooks

## Explanation
- `useMemo` memoizes a computed value, recalculating only when dependencies change.
- `useCallback` memoizes a function, recreating it only when dependencies change.

## Syntax
```jsx
const memoValue = useMemo(() => compute(), [deps]);
const memoCallback = useCallback(() => fn(), [deps]);
```

## Example
```jsx
import React, { useMemo, useCallback, useState } from 'react';

function Example({ num }) {
  const memoValue = useMemo(() => num * 2, [num]);
  const memoCallback = useCallback(() => alert(memoValue), [memoValue]);
  return <button onClick={memoCallback}>Show Double: {memoValue}</button>;
}
``` 