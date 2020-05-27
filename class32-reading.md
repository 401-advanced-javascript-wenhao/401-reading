# Reading 32 - Custom Hooks - 5/26/2020 

## Custom Hooks 
  * Extract duplicated logic from components
  * Share common functionality not state
  * Take advantage of useEffect lifecycle
  * Common use cases - make coding neat and dry
    * Handle Forms
    * Pre-fetch API data
    * Connect to services (socket.io, Q, etc)

## How does custom hooks work
* Hooks are exported as a function, named as `useXXX()`
* Hooks return data or functions that are required to reuse their internal functionality
* Hooks are imported into components
* Components can re-use the hook functionality or data/state as needed
* Hooks do not render 
Example:<br/>
```javascript
// create custom hooks in the use-food-hook.js and export it
export default function useFoodHook(hungry) {
  const foot = 'cookies';
  return hungry ? food : null;
}

// import custom hooks and use it
import useFeedme from 'use-food-hook.js';
const myComponent = props => {
  const food = useFeedMe(true);
  return <div>{food}</div>
}
```