# React.memo, useMemo, useCallback

## Explanation
- `React.memo` memoizes a component, preventing unnecessary re-renders if props don't change.
- `useMemo` memoizes a computed value.
- `useCallback` memoizes a function reference.

## Syntax
```jsx
const Memoized = React.memo(Component);
const memoValue = useMemo(() => compute(), [deps]);
const memoCallback = useCallback(() => fn(), [deps]);
```

## Example
```jsx
import React, { useMemo, useCallback, useState } from 'react';

const MemoChild = React.memo(function MemoChild({ value, onClick }) {
  return <button onClick={onClick}>{value}</button>;
});

function Parent() {
  const [count, setCount] = useState(0);
  const memoValue = useMemo(() => count * 2, [count]);
  const memoCallback = useCallback(() => setCount(c => c + 1), []);
  return <MemoChild value={memoValue} onClick={memoCallback} />;
}
``` 