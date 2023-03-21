# Context API: Behaviors
1. How do useReducer and useContext work together to simplify state management in a React application? (At least two paragraphs of prose.)
- Reducers let you consolidate a component's state update logic
- Context lets you pass info deep down to other components
- You can combine reducer with context to let any component read and update state above it
- Passing down all state and functions through props can be repetitive
- Put state and function into context and this can be read by any child component without the repetitive prop
- Create separate contexts to hold state and to hold the function
```js
  <TasksContext.Provider value={tasks}>
      <TasksDispatchContext.Provider value={dispatch}>
        ...
      </TasksDispatchContext.Provider>
    </TasksContext.Provider>
```
- Any components that need this data can access it through the named context
- They can access state to display the data or access the function to update state

```js
export default function TaskList() {
  const tasks = useContext(TasksContext);
  // ...
```
- You can further declutter the components by moving all wiring into one file