# Reading 31 - Hooks API - 5/25/2020

## Hooks  
* Create and manage state in a function component 
* Hooks are JS functions, but impose additional rules:  
  * Hooks must be named with a `use` prefix
  * Only call Hooks at the top level, not inside loops, conditions, or nested function
  * Only call Hooks from React function components

## Built In Hooks - useState()
Example:<br/>
```javascript
import React, { useState } from 'react';

const Counter = props => {
  const [ clicks, setClicks ] = useState(0);

  return (
    <div>...</div>
  )
}

export default Counter;
```