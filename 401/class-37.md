# Redux - Combined Reducers

### Multiple Reducers Example
1. Why create multiple reducers?
- Multiple reducers can respond to the same action, independently update their slice as needed, and the updated slices are combined into the new state object. 

2. How would you combine multiple reducers?

``` 
export const firstNamedReducer = (state = 1, action) => state

export const secondNamedReducer = (state = 2, action) => state

combineReducers({
  firstNamedReducer,
  secondNamedReducer
})

```

3. How will you manage state as an immutable object? why?
- Immutability of redux state is necessary since it allows detecting redux state changes in an efficient manner. 
- When we want to modify redux state, we create a copy of it and apply modifications to that copy - which then becomes the new state. 


### Redux Docs: Using Combined Reducers
1. `combineReducers` is a utility function to simplify the most common use case when writing `redux reducers`.

2. Explain how `combineReducers` assembles the new state tree.
- It will call each slice reducer with its current slice of state and the current action, giving the slice reducer a chance to respond and update its slice of state if needed. 
- In that sense, `combineReducers` does 'call all reducers', or at least all of the slice reducers it is wrapping. 

3. How would you define initial state in an app using `combineReducers`?
- `createStore` can take `preloadedState` as its second argument. This is primarily intended for initializing the store with state that was previously persisted elsewhere, such as the browser's localStorage. 
- The other way is for the root reducer to return the initial state value when the state argument is `undefined`.

### Redux Docs: Combined Reducer Syntax
1. Why will you want to split your reducing functions as your app becomes more complex?
- If it is more complex, you will want each reducing function to manage independent parts of state. 

2. The `combineReducers` helper function turns an object whose values are different reducing functions into a single reducing function you can pass to `createStore`.
- The resulting reducer calls every child reducer, and gathers their results into a single state object. The state produced by `combineReducers()` namespaces the states of each reducer under their keys as passed to `combineReducers()`.

3. What is a popular convention when naming reducers?
- Naming reducers after the state slice they manage. 