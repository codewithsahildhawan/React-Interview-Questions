# Testing tools (Jest, RTL, etc.)

## Explanation
Jest is a popular testing framework for JavaScript. React Testing Library (RTL) is used for testing React components by simulating user interactions.

## Syntax
```js
// Jest
test('adds numbers', () => {
  expect(1 + 2).toBe(3);
});
// RTL
import { render, screen } from '@testing-library/react';
render(<Component />);
```

## Example
```jsx
// Jest
test('adds numbers', () => {
  expect(1 + 2).toBe(3);
});

// RTL
import React from 'react';
import { render, screen } from '@testing-library/react';

function Hello() {
  return <h1>Hello</h1>;
}

test('renders hello', () => {
  render(<Hello />);
  expect(screen.getByText('Hello')).toBeInTheDocument();
});
``` 