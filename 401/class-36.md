# Application State with Redux 

### Dan Abramov Redux Tutorials

- Redux provides a solid, stable, and mature solution to managing state in your React app. 
1. What is the first principle of Redux?
- The single immutable state tree. You can represent the whole state of your app as a single object. 

2. What is a store and what do we use our reducers for within that store?
- A store holds the whole state tree of your app. The only way to change the state inside it is to dispatch an action on it. 
- When you create it, you need to specify the reducer that tells how state is updated with actions. 

3. Name three Redux store methods given to us by createStore and describe their use.
- getState()
    - Returns the current state tree of your app. It is equal to the last value returned by the store's reducer. 
- dispatch(action)
    - Dispatches an action. This is the only way to trigger a state change. 
    - The store's reducing function will be called with the current getState() result and the given `action` synchronously. 
    - action: a plain object describing the change that makes sense for you app. 
- subscribe(listener)
    - Adds a change listener. It will be called any time an action is dispatched, and some part of the state tree may potentially have changed. You may call getState() to read the current state tree inside the callback. 

4. Explain to a non-technical recruiter what combineReducers() does and why it is useful.
- The `combineReducers` helper function turns an object whose values are different reducing functions into a single reducing function you can pass to `createStore`. 
- The resulting reducer calls every child reducer and gathers their results into a single state object. 