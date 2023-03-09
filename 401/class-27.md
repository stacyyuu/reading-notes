# UseState() Hook

### Introducing Hooks
1. What was the motivation for introducing Hooks?
- To solve a variety of problems in React. 
- With Hooks, you can extract stateful logic from a component so that it can be tested independently and reused. 
- Hooks let you split one component into smaller functions based on what pieces are related, rather than forcing a split based on lifecycle methods. 

2. What changes are important regarding implementing Hooks versus Component Classes?
- Hooks let use state and other React features without writing a class. 

3. Hooks allow you to reuse stateful logic without changing your component hierarchy. This makes it easy to share Hooks among many components or with the community. 

### Hooks API
1. Name two rules imposed by React Hook usage.
- Hooks are like JS functions, but impose two additional rules:
- Only call Hooks at the top level, not inside loops, conditions, or nested functions.
- Only call Hooks from React function components, not inside JS functions. 

2. How would you identify a custom Hook and why might you create one?
- Using a custom Hook allows you to reuse stateful logic between components without adding more components to your tree. 
- Although the stateful logic can be reused, the state itself is independent in each component. 

### The State Hook
- Count state hook: `  const [count, setCount] = useState(0);`
1. What is a Hook?
- A Hook is a special function that lets you 'hook into' React futures. 
- It lets you add React state into function components by adding `useState`. 

2. When would I use the useState Hook?
- If you are writing a function component and need to add state into it. 

3. If you were to add React state to a function component by declaring a state variable:
4. What does calling useState do?
- It declares a 'state variable'. 
- It is a new way to use the same exact capabilities that `this.state` provides in a class. 
- It is a way to 'preserve' some values between the function calls. 

5. What do we pass to useState as an argument?
- The only argument passed is the initial state. 
- It does not have to be an object. 

6. What does useState return?
- It returns a pair of values: the current state and a function that updates it. 