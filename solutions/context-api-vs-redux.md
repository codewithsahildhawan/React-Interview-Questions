# Context API vs Redux

## Explanation
The Context API is built into React for simple global state sharing. Redux is a third-party library for more complex state management with middleware, devtools, and advanced patterns.

## Syntax
```jsx
// Context API
const MyContext = React.createContext();
<MyContext.Provider value={...}>
  <Child />
</MyContext.Provider>
// Redux
import { Provider } from 'react-redux';
<Provider store={store}>
  <App />
</Provider>
```

## Example
```jsx
// Context API
import React, { createContext, useContext } from 'react';
const MyContext = createContext('default');
function Child() {
  const value = useContext(MyContext);
  return <div>{value}</div>;
}
function Parent() {
  return <MyContext.Provider value="shared"><Child /></MyContext.Provider>;
}

// Redux (simplified)
import React from 'react';
import { Provider, useSelector, useDispatch } from 'react-redux';
import { createStore } from 'redux';
const reducer = (state = { count: 0 }, action) =>
  action.type === 'inc' ? { count: state.count + 1 } : state;
const store = createStore(reducer);
function Counter() {
  const count = useSelector(s => s.count);
  const dispatch = useDispatch();
  return <button onClick={() => dispatch({ type: 'inc' })}>{count}</button>;
}
function App() {
  return <Provider store={store}><Counter /></Provider>;
}
``` 