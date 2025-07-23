# Create a lazy loaded component in React

## Explanation
React supports lazy loading components using `React.lazy` and `Suspense`. This helps split code and load components only when needed.

## Syntax
```jsx
import React, { Suspense, lazy } from 'react';
const LazyComponent = lazy(() => import('./LazyComponent'));

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