# How to display number of characters remaining functionality for textarea using react useRef?

## Explanation
You can use `useRef` to access the textarea and state to track the number of characters remaining.

## Syntax
```jsx
const ref = useRef();
<textarea ref={ref} onChange={...} />
<p>{maxLength - value.length} characters remaining</p>
```

## Example
```jsx
import React, { useRef, useState } from 'react';

function CharCountTextarea() {
  const [text, setText] = useState('');
  const maxLength = 100;
  const textareaRef = useRef(null);
  return (
    <div>
      <textarea
        ref={textareaRef}
        maxLength={maxLength}
        value={text}
        onChange={e => setText(e.target.value)}
      />
      <p>{maxLength - text.length} characters remaining</p>
    </div>
  );
}
``` 