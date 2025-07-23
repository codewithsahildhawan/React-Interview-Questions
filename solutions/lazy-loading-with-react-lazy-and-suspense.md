# Lazy loading with React.lazy & Suspense

## Explanation
`React.lazy` and `Suspense` allow you to load components only when needed, reducing initial bundle size.

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