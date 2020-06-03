# Reading 37 - Redux: Combined Reducers - 6/2/2020  

## Combined Reducers  
* Nothing more than pulling in more than one reducers from source and creating a keyed object from them 
* Any component can reach into the store and use state  

## What's the point of combined reducers? 
* Obey the single responsibility principle (single source of truth) 
  * Each reducer really should have only 1 part of state to manage  
  * Is this more work/boilerplate? Yes
  * Does it allow you decouple logic? Yes 

## What about the actions?  
* Each reducer technically has its own actions and creators 
* However, they can cross over and both be dispatched 
  * Example: 
  ```javascript
  // counter-store.js
  export default function reducer (state = initialState, action) {
    const { type, payload } = action;
    switch(type) {
      case 'INCREMENT':
        return { value: state.value + 1 };
      
      case 'RESET':
        return { value: 0 };

      default:
        return state;
    }
  }


  // history-store.js
  export default (state = initialState, action) => {
    const { type, payload } = action;
    switch(type) {
      case: 'CLICK':
        return { clicks: state.clicks + 1 };

      case: 'RESET':
        return { clicks: 0 };
      
      default:
        return state;
    }
  }
  ```