# What are React Fragments and their performance benefits?

## Explanation
React Fragments let you group multiple elements without adding extra nodes to the DOM, improving performance and cleaner markup.

## Syntax
```jsx
<>
  <Child1 />
  <Child2 />
</>
```

## Example
```jsx
import React from 'react';

function List() {
  return (
    <>
      <li>Item 1</li>
      <li>Item 2</li>
    </>
  );
}
``` 