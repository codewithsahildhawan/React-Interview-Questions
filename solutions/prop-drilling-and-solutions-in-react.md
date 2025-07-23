# Prop drilling & solutions

## Explanation
Prop drilling is passing data through many layers of components. Solutions include using the Context API or state management libraries to avoid deeply nested props.

## Syntax
```jsx
// Prop drilling
<Parent value={...} />
// Context API
const MyContext = React.createContext();
<MyContext.Provider value={...}><Child /></MyContext.Provider>
```

## Example
```jsx
import React, { createContext, useContext } from 'react';
const MyContext = createContext('default');
function Child() {
  const value = useContext(MyContext);
  return <div>{value}</div>;
}
function Parent() {
  return <MyContext.Provider value="shared"><Child /></MyContext.Provider>;
}
``` 