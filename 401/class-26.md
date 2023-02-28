# Component Based UI

### React - Hello World 
1. What are the building blocks of a React app?
- Elements and components. 

2. What is the difference between an element and a React component?
- Elements are the smallest building blocks of React. They are what components are made of. 
- An element is a plain object that describes what we want to appear in terms of the DOM nodes. <br>
`const element = <h1>Hello, world</h1>;`
- Conceptually, components are like JS functions. They accept inputs (called 'props') and return React elements describing what should appear on the screen. <br>
`function Welcome(props) {` <br>
  `return <h1>Hello, {props.name}</h1>;` <br>
`}`

3. What are some advantages of React’s component based architecture?
- Components let you split the UI into independent, reusable pieces, and think about each piece in isolation. 

### Introducing JSX 
1. What is JSX and why do we use it?
- JSX is a syntax extension to JS. It is recommended using it with React in order to describe what the UI should look like. 
- JSX produces React 'elements'. 

2. Describe the process of embedding JavaScript expressions in JSX.
- Functions and variables can be embedded into elements by wrapping them in curly brackets. 
- You can put any valid JS expression inside the curly braces in JSX. <br>
`function formatName(user) {`
  `return user.firstName + ' ' + user.lastName;`
`}`
<br><br>
`const user = {`
  `firstName: 'Harper',`
  `lastName: 'Perez'`
`};`
<br><br>
`const element = (`
  `<h1>`
    `Hello, {formatName(user)}!`
 ` </h1>`
`);`

3. Is it safe to embed user input in JSX? Explain.
- Yes. By default, React DOM escapes any values embedded in JSX before rendering them. Thus it ensures that you can never inject anything that's not explicitly written in your app. 
- Everything is converted to a string before being rendered. 

### Rendering Elements
1. Explain what a React Component is to a non-technical friend.
- Independent and reusable bits of code. 
- Similar to JS functions, but work in isolation and return HTML.
- Class components and Function components. 

2. Describe mutability and React Components, specifically, how is the UI updated?
- React elements are immutable. Once it is created, its children or attributes can't be changed. 
- Acts like a single frame in a movie and represents the UI at a certain point in time.
- The only way to update UI is to create a new element and pass it to `root.render()`.

3. If changes are made to the UI, what does React update?
- React DOM compares the element and children to the previous one and only applies the DOM updates necessary to bring the DOM to the desired state. 
