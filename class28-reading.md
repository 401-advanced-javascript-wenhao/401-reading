# Reading 28 - Props and State - 5/20/2020  

## Forms and Inputs 
* React forms maintain internal state
* React inputs are stateful child components
* Manage the state of inputs through own stateful component and one way data binding
* Each input has an `onChange` event - update form state when user interacts with an input

## Props  
* Arbitrary inputs - can be data or function
* Get passed to children components
* Owned by a parent
* Immutable (read-only)
* Available on the context by using `this.props`

## State
* Internal within component
* Managed at App level
* Single source of truth

## One way data flow
* State can only be passed from parent component to a child component through the use of props
* If a child wants to pass some data to a parent: 
  * The parent can pass a function to the child through props
  * The child invoke the function and the function will update the state  