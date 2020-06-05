# Reading 39 - Redux Toolkit - 6/4/2020 

## Redux Toolkit - build and manage a Redux store 
* Introduced by Redux developer team  
* Specifies a few different means of building a reducer and action set that work well together and are easier to understand and integrate 
* Example:  
```javascript
const postsSlice = createSlice({
  name: 'posts',
  initialState: [],
  reducers: {
    createPost(state, action) {},
    updatePost(state, action) {},
    deletePost(state, action) {}
  }
})

// Extract the action creators object and the reducer 
const { actions, reducer } = postsSlice;
// Extract and export each action creator by name
export const { createPost, updatePost, deletePost } = actions;
// Export the reducer, either as a default or named export
export default reducer;

// ----- Sample Use -----
console.log(createPost({ id:123, title: 'Hello World }));

{type: "posts/createPost", payload: {id: 123, title: "Hello World"}}

// Notice how createSlice transforms your definition.
console.log(postSlice);
{ name: 'posts', actions: { createPost, updatePost, deletePost }, reducer}
```