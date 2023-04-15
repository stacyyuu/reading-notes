# Redux - Additional Topics

### Redux Toolkit

1. What concerns are addressed by Redux Toolkit?

- Standard way to write Redux logic.
- It includes a powerful data fetching and caching capability that is dubbed 'RTK Query'. 
- Addresses three common concerns:
  - 'Configuring a Redux store is too complicated'
  - 'I have to add a lot of packages to get Redux to do anything useful'
  - 'Redux requires too much boilerplate code'

2. What does `configureStore()` do?
- Wraps `createStore` to provide simplified configuration options and good defaults. It can automatically combine your slice reducers, adds whatever Redux middleware you supply, includes `redux-thunk` by default, and enables use of Redux DevTools Extension. 

3. How would I use `createSlice()`?
- Accepts an object of reducer functions, a slice name, and an initial state value. Automatically generates a slice reducer with corresponding action creators and action types. 

### MobX

1. What is Mobx?
- Simple, scalable, and battle testes state management solution. 
- Standalone library that is commonly used with React. 

2. How does MobX make it “impossible” to produce an inconsistent state?
- Making sure that everything can be derived from the application state. 

![MobX Spreadsheet](https://mobx.js.org/assets/getting-started-assets/overview.png)

3. How would we build a reactive user interface?
- The `observer` HoC wrapper from `mobx-react-lite` fixes that by wrapping the React component in `autorun`.
- This keeps the component in sync with state and individually re-renders when relevant data changes. 
