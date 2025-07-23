# What is code splitting and how to implement it?

## Explanation
Code splitting is breaking up your code into smaller bundles that are loaded on demand. In React, use `React.lazy` and `Suspense` for component-level code splitting.

## Syntax
```jsx
const LazyComponent = React.lazy(() => import('./LazyComponent'));
<Suspense fallback={<div>Loading...</div>}>
  <LazyComponent />
</Suspense>
```

## Example
```jsx
import React, { Suspense, lazy } from 'react';

const UserProfile = lazy(() => import('./UserProfile'));

function App() {
  return (
    <Suspense fallback={<div>Loading...</div>}>
      <UserProfile />
    </Suspense>
  );
}
``` 