# How to optimize bundle size in React?

## Explanation
Optimize bundle size by using code splitting, tree shaking, dynamic imports, and removing unused code. Tools like webpack-bundle-analyzer help analyze bundle size.

## Syntax
```js
// Dynamic import
const LazyComponent = React.lazy(() => import('./LazyComponent'));
```

## Example
```js
// In webpack.config.js
optimization: {
  splitChunks: { chunks: 'all' },
},
// In React
import React, { Suspense, lazy } from 'react';
const LazyComponent = lazy(() => import('./LazyComponent'));
``` 