## Readings: React and Forms

### Our reading today is based on React Forms and The Conditional Operator. 
---

## React Docs - Forms
1. What is a ‘Controlled Component’?
- In HTML, form elements such as `<input>, <textarea>, <select>` typically maintain their own state and update it based on user input. 
- In React, mutable state is typically kept in the state property of components, and only updated with setState().
- We can combine the two by making the React state be the "single source of truth". Then the React component that renders a form also controls what happens in that form on subsequent user input. 
- An input form element whose value is controlled by React in this way is called a 'controlled component'.

2. Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.
- The user responses can be updated in state while they are entered. 
- If they are submitted then you have to add an event handler to the onSubmit button in order to prevent default, aka refreshing the page. 

3. How do we target what the user is entering if we have an event handler on an input field?
- In order to target the user input, we set the state to the event.target.value. 
- `<input type = 'text' value = {this.state.value} onChange = {this.setState({value: event.target.value})}>`

## The Conditional (Ternary) Operator Explained

1. Why would we use a ternary operator?
- Shorten your `if` statements into one line of code with the conditional operator 
- `condition ? value if true: value if false`
- `condition` is what's being tested
- `?` separates our conditional from our **true** value. 
- `:` if you condition evals false, any code after colon is executed. 

2. Rewrite the following statement using a ternary statement:
- `x === y ? console.log(true) : console.log(false);`

[Back to main page](README.md)