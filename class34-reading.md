# Reading 34 - `<Login />` and `<Auth />` 

## Authentication + Role Based Authorization  
Problems need to solve: 
* Is this a valid user (are they logged in)?
* What is the user authorized to do?  
  * Which parts of our application care about this? 
  * How can we determine this?  
    * What's in the token?  
    * Contact between the UI and the API  
* How do we make this easy to use?  

## Proposal 
* Use `<Auth />` component  
* Conditionally render componenets based on user's permissions and login status 
* Must not use Redux - we don't want to force implementors into a specific state management system  
```javascript
// The div only shows if users are logged in
<Auth>
  <div />
</Auth>

// The div only shows if users are logged in and have read permissions
<Auth capability="read">
  <div />
</Auth>
```