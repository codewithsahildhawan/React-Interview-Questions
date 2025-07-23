# How to display data entered by the user in another textbox?

## Explanation
You can use React state to capture user input from one textbox and display it in another textbox by binding the value to state.

## Syntax
```jsx
const [value, setValue] = useState('');
<input value={value} onChange={e => setValue(e.target.value)} />
<input value={value} readOnly />
```

## Example
```jsx
import React, { useState } from 'react';

function MirrorInput() {
  const [text, setText] = useState('');
  return (
    <div>
      <input value={text} onChange={e => setText(e.target.value)} placeholder="Type here" />
      <input value={text} readOnly placeholder="Mirrored here" />
    </div>
  );
}
``` 