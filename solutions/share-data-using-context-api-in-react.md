# Share data between components using context API?

## Explanation
The Context API allows you to share data globally across components without prop drilling. Create a context, provide a value, and consume it in child components.

## Syntax
```jsx
const MyContext = React.createContext();
<MyContext.Provider value={...}>
  <Child />
</MyContext.Provider>
// In child
const value = useContext(MyContext);
```

## Example
```jsx
import React, { createContext, useContext } from 'react';

const ThemeContext = createContext('light');

function Child() {
  const theme = useContext(ThemeContext);
  return <div>Theme: {theme}</div>;
}

function Parent() {
  return (
    <ThemeContext.Provider value="dark">
      <Child />
    </ThemeContext.Provider>
  );
}
``` 