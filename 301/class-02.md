## Readings: State and Props

### Our reading today is based on React lifecycle and React state Vs props. 
---

## React Lifecycle

- React lets you define components as classes or functions.
- Methods you are able to use on these are called lifecycle events.
- These methods can be called during the lifecycle of a component, and they allow you to update the UI and app states. 
- Mounting, Updating, and Unmounting are the three phases of the component lifecycle. 

1. Based off the diagram, what happens first, the ‘render’ or the ‘componentDidMount’?
- Render happens first before componentDidMount. 
<img src= "https://miro.medium.com/max/2400/0*0saPKFiTUk6W3FYp">

2. What is the very first thing to happen in the lifecycle of React?
- **Mounting**: Instance of component being created and inserted into DOM, this occurs during mounting phase. 
- `Constructor, static getDerivedStateFromProps, render, componentDidMount, and UNSAFE_componentWillMount` all occur in this order during mounting. 
- **Updating**: Anytime component is updated or state changes then it is rerendered. These lifecycle events happen during updating in this order. 
- `static getDerivedStateFromProps, shouldComponentUpdate, render,`
`getSnapshotBeforeUpdate, componentDidUpdate, UNSAFE_componentWillUpdate, UNSAFE_componentWillReceiveProps.`
- **Unmounting**: Final phase of lifecycle called when component is being removed from DOM. 
- `componentWillUnmount` is the only lifecycle event during this phase.

3. Put the following things in the order that they happen: `componentDidMount, render, constructor, componentWillUnmount, React Updates`
- `constructor, render, componentDidMount, React Updates, componentWillUnmount`.

4. What does `componentDidMount` do?
- This method is invoked immediately after component is mounted. If you need to load anything using a network request or initialize the DOM, it should go here. This method is a good place to set up any subscriptions. If you do that, don't forget to unsubscribe in componentWillUnmount().
- setState() can be called here, but should be used sparingly because it will cause rerender, which can lead to performance issues. 

## React State Vs Props
1. What types of things can you pass in the props?
- Think of as 'arguments to a function'. When you create a component and want to render it, you will pass in the props you want to give to it. 
- What you want to initialize your component to or what you want your component to render like. 
2. What is the big difference between props and state?
- State is something handled inside a component and can be updated inside the component. Props is something you pass into a component and must be updated outside of the component. 
- Props initializes our counter number while our state increases or decreases that count, depending on what the component is being used for. 
3. When do we re-render our application?
- When you change the state inside of your app, it will re-render that section of your app. 
- Props can't be changed inside, but outside the component. 
- If component does not need to be changed, it will most likely not need a state. It will just display its props. 
4. What are some examples of things that we could store in state?
- Useful when you need to actually rerender and update your app based on something the user has done.
- Anything that wants to be changed in your app, needs to be stored in the state. 
- State is useful inside of a form, to store what they're updating the value of the form to. 
- Props are useful when you want to display info inside a component without hardcoding it. Essentially, a variable to a function. 

[Back to main page](README.md)