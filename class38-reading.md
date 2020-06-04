# Reading 38 - Redux: Asynchronous Actions - 6/3/2020 
Redux middleware provides the mechanism to work asynchronously with Redux

## Thunking for Data  
* Sometimes we need to do some asynchronous action before we dispatch it to the reducer. For example: get something from a remote api 
```javascript
const api = 'https://api.mockable.io/api/v1/stuff';

export const get = () => {
  return utils.fetchData(api)
    .then(records => {
      dispatch(getAction(records));
    });
};

const getAction = payload => {
  return {
    type: 'GET',
    payload: payload
  };
};
```

* Thunk middleware  
```javascript
export default store => next => action =>
  typeof action === 'function' ? action(store.dispatch, store.getState) : next(action);
```
  * Middleware is a curried function that evaluates the action
    * Either a function gets invoked with the store's `dispatch()` and `getState()` methods or
    * It simply runs the action created by a normal action creator