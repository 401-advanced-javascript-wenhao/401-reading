# Reading 36 - Redux - 6/1/2020 

## Redux - managing state tool  
Redux is a library that specializes in sharing state between coomponents using a global "store". 3 distinct aspects make a `store`:<br/>
* State 
* Reducers (strategies to alter state)  
* Action (methods that get "dispatched" or "run", which trigger associated reducers)  

## Redux Store  
* Where application state is stored 
* Identify various reducers and middleware that need to be made available and used globally 
* React uses "reducers" to hold and manage state
* Reducer manage just one part of the larger application state 
* Reducer creates an initial "empty" state and then evaluates action and make a copy of state accordingly  
* Reducers hear the "dispatch" and "payload"  

## How does redux work  
* Action: an object with a type and payload 
* Action creators: functions that retun an action 
* Reducers: evaluate the "type" property on an action and makes a copy of the state, given the payload  
* Reducers get included into the creation of store - the single object of tree holding in the app) with `createStore(reducer)`  
* Application access this state through use of a `react-redux` npm module that gives us a `<Provider` component 
* `<Provider>` component has a prop called `store` that takes in the state and feeds it to our entire app

