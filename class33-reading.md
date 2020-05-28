# Reading 33 - Context API - 5/27/2020  

## Context  
* A mean of passing state down the component tree through a Provider/Consumer relationship  
* At the high level, a `Provider` can make its state available, along with means of altering it (methods)  
* At the lower level, any component can opt-in and become a `Consumer` and receive this.state from context  

## How to implement it  
* In a class style component, there are 2 ways to attach to context 
  1. wrapper and use a `get` function to pull in context  
  2. statically declare a connection to the context provider and then use `this.context` to connect to state from the context provider  
* In a function component, you can use the `useContext()` hook to tap right in. It returns and provides access to whatever context provider exports 
