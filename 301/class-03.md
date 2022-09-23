## Readings: Passing Functions as Props

### Our reading today is based on React Docs - List and Keys, and the Spread Operator. 
---

## React Docs - List and Keys

1. What does .map() return?
- .map() creates a new array populated with results of calling a provided function on every element in the calling array. 
- Similar to .forEach(), but it will always return a new array of same length of original array.
- It does not mutate the original array. 
2. If I want to loop through an array and display each value in JSX, how do I do that in React?
- You can use the .map() function. 
- You can build collections of elements and include them in JSX using curly braces {}.
3. Each list item needs a unique ____.
- Key. A 'key' is a special string attribute you need to include when creating list of elements. 
- `<li key = >`
4. What is the purpose of a key?
- Keys help React identify which items have changed, are added, or are removed. 
- Keys should be given to the elements inside the array to give the elements a stable identity. 
- The best way to pick a key is to use a string that uniquely identifies a list item among its siblings. 
- Most often you would use IDs from your data as keys. 
- `<li keys = {todo.id}>`
- When you don't have stable IDs for rendered items, you may use the item as index as a key as last resort. This is not recommended if order of items may change. 
- `<li keys = {index}>`

## The Spread Operator

1. What is the spread operator?
- Useful and quick syntax for adding items to arrays, combining arrays or objects, and spreading an array out into a function's argument. 
- In JS, spread syntax refers to use of ellipsis of three dots `(...)` to expand an iterable object into list of arguments. 
- When `...arr` is used in function call, it expands an iterable object `arr` into list of arguments. 
- Spread operator was added to JS in ES6. 

2. List 4 things that the spread operator can do.
- Spread syntax 'spreads' the an array into separate arguments when passing an array into a JS function. 
- `Math.max(...[1, 2, 3]);` 
- The spread operator is useful for many different routine tasks in JS including:
- Copying an array, concatenating or combining arrays, using math functions, using an array as an argument, adding an item to a list, adding to state in React, combining objects, and converting NodeList to an array. 

3. Give an example of using the spread operator to combine two arrays.
- `const ourArray = [...myArray, ...yourArray];`

4. Give an example of using the spread operator to add a new item to an array.
- `const fewMoreFruit = ['watermelon', 'pineapple', ...fewFruitArray];`

5. Give an example of using the spread operator to combine two objects into one.
- `const objectThree = {...objectOne, ...objectTwo, hello: 'world'};`

## How to Pass Functions Between Components

1. In the video, what is the first step that the developer does to pass functions between components?
- State exists at higher component, lower component triggers something to happen at that state.
- Create function at wherever the state is that we're going to change.

2. In your own words, what does the increment function do?
- The increment function updates the count based on the name that is passed from the object. 

3. How can you pass a method from a parent component into a child component?
- Create a new prop name and assign with this.method. It references the method that exists in the component object. 
- `increment = {this.increment}`
- It can be passed just like a prop. 

4. How does the child component invoke a method that was passed to it from a parent component?
- It can then be called on the separate component by using this.props.methoc().

[Back to main page](README.md)