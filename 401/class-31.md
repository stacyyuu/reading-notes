# Context API

### Context API
1. What can React Context provide your app?
- Context provides a way to pass data through the component tree without having to pass props down manually at every level. 
- It is designed to share data that can be considered 'global'. 

2. Why might we use Context?
- When we want to pass data from one component to another. 

3. Why should we use it sparingly?
- It is primarily used when data needs to be accessible to many components. It can make component reuse more difficult if not used sparingly.
- If you want to avoid passing data through many levels, component composition is often a simpler solution than context. 

### Awesome React Context Links
1. Consume content from (at least) two of the Awesome React Context links. Share your take-away from each:
    - Takeaway 1: 
    
    Constate - We can break React Context API into three parts: `Context`, `Provider`, and `Consumer`. 
    ```js
    const Context = createContext()
    ```
    Context is created and then Provider. Provider uses `Context.Provider` and passes `state` and `setState` down. Our `Consumer` needs to use `Context.Consumer` to access `state` and `setState` passed by `Provider`. The final step is to wrap our app with `Provider`. 

    - Takeaway 2: 

    The consumer must have access to the same Context component - if you were to create a new context, with the same parameter as input, a new Context would be created and the data would not be passed. 