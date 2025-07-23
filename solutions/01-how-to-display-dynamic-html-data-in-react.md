# How to display dynamic HTML data in React?

## Explanation
In React, you can display dynamic HTML data by using JSX expressions and state/props. For raw HTML, use the `dangerouslySetInnerHTML` attribute, but be cautious as it can expose your app to XSS attacks.

## Syntax
```jsx
// Using JSX for dynamic data
<div>{dynamicValue}</div>

// Rendering raw HTML (use with caution)
<div dangerouslySetInnerHTML={{ __html: htmlString }} />
```

## Example
```jsx
import React, { useState } from 'react';

function DynamicHtmlExample() {
  const [htmlString, setHtmlString] = useState('<b>Hello, <i>World!</i></b>');
  return (
    <div>
      <h3>Dynamic HTML with JSX:</h3>
      <div>{'This is a dynamic value'}</div>
      <h3>Dynamic HTML with dangerouslySetInnerHTML:</h3>
      <div dangerouslySetInnerHTML={{ __html: htmlString }} />
    </div>
  );
}
``` 