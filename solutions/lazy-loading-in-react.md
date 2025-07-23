# What is lazy loading and how to implement it?

## Explanation
Lazy loading loads components or images only when needed. In React, use `React.lazy` and `Suspense` for components, or Intersection Observer for images.

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