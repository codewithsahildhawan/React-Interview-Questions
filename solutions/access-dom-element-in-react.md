# How do you access the DOM element?

## Explanation
In React, you can access a DOM element using the `ref` attribute. In functional components, use the `useRef` hook to create a reference and attach it to the element.

## Syntax
```jsx
import React, { useRef } from 'react';

const myRef = useRef(null);
// ...
<input ref={myRef} />
```

## Example
```jsx
import React, { useRef } from 'react';

function FocusInput() {
  const inputRef = useRef(null);
  const focusInput = () => inputRef.current.focus();
  return (
    <div>
      <input ref={inputRef} type="text" />
      <button onClick={focusInput}>Focus Input</button>
    </div>
  );
}
``` 