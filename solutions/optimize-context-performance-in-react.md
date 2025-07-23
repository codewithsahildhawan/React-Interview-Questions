# How to optimize React Context performance?

## Explanation
To optimize Context performance, split contexts, memoize context values, and avoid unnecessary provider re-renders.

## Syntax
```jsx
const value = useMemo(() => ({ ... }), [deps]);
<MyContext.Provider value={value}>
  <Child />
</MyContext.Provider>
```

## Example
```jsx
import React, { createContext, useMemo, useState } from 'react';

const ThemeContext = createContext();

function App() {
  const [theme, setTheme] = useState('light');
  const value = useMemo(() => ({ theme, setTheme }), [theme]);
  return (
    <ThemeContext.Provider value={value}>
      <Toolbar />
    </ThemeContext.Provider>
  );
}

function Toolbar() {
  return <ThemeButton />;
}

function ThemeButton() {
  const { theme, setTheme } = React.useContext(ThemeContext);
  return (
    <button onClick={() => setTheme(t => t === 'light' ? 'dark' : 'light')}>
      Current theme: {theme}
    </button>
  );
}
``` 