# Advanced State With Reducers

### useReducer Hook
1. Name an alternative to the useState Hook.
- An alternative to useState is `useReducer`. 
- `(state, action) => newState` and returns the current state paired with a `dispatch` method. 

2. Why might the useReducer Hook be preferable to the useState Hook?
- It is usually preferable when you have a complex state logic that involves multiple sub-values or the state depends on the previous one. 
- It also lets you optimize performance for components that trigger deep updates because you can pass dispatch down instead of callbacks. 

3. What are two ways to set the initial state?
- Simplest: Pass initial state as a second argument. 
- Laziest: Pass `init` function as the third argument. 
- `init(initialArg)`

### Ultimate Guide to useReducer

1. In terms of state, what does useReducer expect to receive as a parameter?
- It accepts a reducer function as its first parameter and the initial state as second. 
- `const initialState = { count: 0 }` <br>
 `const [state, dispatch] = useReducer(reducer, initialState)`

2. What does useReducer return?
- It returns an array that holds the current state value and a `dispatch` function to which you can pass an action and later invoke it. 

3. Explain dispatch to a non-technical recruiter.
- The `dispatch` function accepts an object that represents the type of action we want to execute when it is called. 
- It sends the type of action to the reducer function to preform its job, which is updating the state. 