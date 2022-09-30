## Readings: Putting It All Together

### Our reading today is based on Thinking in React and Higher-Order Function. 
---

## React Docs - Thinking in React 
1. What is the `single responsibility principle` and how does it apply to components?
- This technique helps you decide what should be its own component. You use this principle if a component should ideally only do one thing. 
- If it ends up growing, it should be decomposed into smaller subcomponents. 
- Since you're often displaying a JSON data model to a user, you'll find that if your model was built correctly, your UI (and therefore your component structure) will map nicely. 
- That's because UI and data models tend to adhere to the same *information architecture*. 
- Separate your UI into components, where each component matches one piece of your data model. 
- Now that we've identified the components in our mock, arrange them into a hierarchy. 
- Components that appear within another component in the mock should appear as a child in hierarchy. 

2. What does it mean to build a ‘static’ version of your application?
- Now that you have your component hierarchy, it's time to implement your app. The easiest way is to build a version that takes your data model and renders the UI but has no interactivity. 
- It's best to decouple these processes because building a static version requires a lot of typing and no thinking, and adding interactivity requires a lot of thinking and not a lot of typing. 

3. Once you have a static application, what do you need to add?
- You will want to build components that reuse other components and pass data using *props*.
- *props* are a way of passing data from parent to child. 
- If you're familiar with the concepts of *state*, **don't use state at all** to build this static version. 
- State is reserved only for interactivity, that is, data that changes over time. 
- Since this a static version of the app, you don't need it. 
- You can build top-down or bottom-up following the hierarchy. 
- At the end of this step, you'll have a library of reusable components that render your data model. 
- The components will only have `render()` methods since this is a static version. 
- The component at the top will take your data model as a prop. 

4. What are the three questions you can ask to determine if something is state?
- To make your UI interactive, you need to be able to trigger changes to your underlying data model. 
- React achieves this with **state**.
- Figure out the absolute minimal representation of state your app needs and compute everything else you need on-demand. 
- Ask three questions:
- Is it passed in from a parent via props? If so, it probably isn't state.
- Does it remain unchanged over time? If so, it probably isn't state. 
- Can you compute it based on any other state or props in your component? If so, it isn't state. 

5. How can you identify where state needs to live?
- For every piece of state in your app:
- Identify every component that renders something based on that state.
- Find a common owner component (a single component above all the components that need the state in the hierarchy).
- Either the common owner or another component higher up in the hierarchy should own the state.
- If you can't find a component where it makes sense to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common owner component. 
-  You will then work on handling the components that will need to update state. 

## Higher-Order Functions
1. What is a “higher-order function”?
- Functions that operate on other functions, either by taking them as arguments or by returning them, are called *higher-order functions*.
- Higher-order functions allow us to abstract over *actions*, not just values. They come in several forms:
- Functions that create new functions, functions that change other functions, or functions that provide new types of control flow. 

2. Explore the `greaterThan` function as defined in the reading. In your own words, what is line 2 of this function doing?
- `function greaterThan(n) {`<br>
 ` return m => m > n;`<br>
`}`<br>
`let greaterThan10 = greaterThan(10);`<br>
`console.log(greaterThan10(11));`<br>
`// → true`
- It is assigning greaterThan10 the the function greaterThan with an argument of 10. 
- It then logs the variable with another argument of 11. 
- This returns `m => 11 > 10 = true.`

3. Explain how either `map` or `reduce` operates, with regards to higher-order functions.
- `.map()` is a standard array method.
- This method transforms an array by applying a function to all of its elements and building a new array from the returned values. 
- The new array will have the same length as the input array, but its contents will have been *mapped* to a new form by the function. 
- `.reduce()` is also a standard array method.
- Reduce allows you to compute a single value from an array. 
- It builds a value by repeatedly taking a single element from the array and combining it with the current value. 

[Back to main page](README.md)