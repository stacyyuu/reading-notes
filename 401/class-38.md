# Redux - Async Actions

### Async Actions
1. Why use Redux middleware?
- Reducers cannot contain 'side effects'.
- A 'side effect' is any change to state or behavior that can be seen outside of returning a value from a function. 
- Redux middleware allows us to write async logic that interacts with the Redux store. 
- It is possible to write a middleware function that lets us pass a function to dispatch instead of an action object. 

2. Consider the Redux Async Data Flow Diagram. Describe the flow in your own words.
- A user creates an event by clicking a button. 
- Dispatch is called and we pass in a value that a middleware can look for. 
- When that value reaches middleware, it can make an async call, and then dispatch a real action object when the async call is complete.

3. How are we accommodating async in our Redux app?
- Redux 'Thunk' middleware allows us to write functions that have async logic. That logic can dispatch actions and read the store state as needed. 

### Thunk Middleware
1. Why would you need redux-thunk middleware?
- With a basic Redux store, you can only do simple synchronous updates by dispatching an action.
- Thunk extends the abilities and allows you to write async logic that interacts with the store. 

2. Redux Thunk middleware allows you to write action creators that return a function instead of an action.

3. Describe how any return value from the inner thunk function will be made available.
- Any return value from the inner function will be available as the return value of `dispatch` itself. 
- This is convenient for creating an asynchronous control flow with thunk action creators dispatching each other and returning Promises to wait for each other's completion. 