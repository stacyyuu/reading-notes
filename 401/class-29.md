# Component Lifecycle/useEffect Hook

### useEffect Hook

1. What purpose does useEffect serve in a function component compared to its counterpart(s) in class components?
- The Effect Hook lets you perform side effects in function components.
- It is combination of `componentDidMount`, `componentDidUpdate`, and `componentWillUnmount` combined - the React class lifecycle methods. 
- There are two common side effects in React components: those that require clean up and those that don't aka running code after React has updated the DOM. 

2. When using the useEffect Hook:
    - What does useEffect do?
      - It will call the function that was passed after performing the DOM updates.
    - Why is useEffect called inside a component?
      - It lets us access state variables and props inside the component. 
    - useEffect runs after every render. By default, it runs after the first render and after every update. 
    - Every time we re-render, we schedule a different effect, replacing the previous one. Each effect 'belongs' to a particular render. 

3. Explain the importance of properly implementing effects with Cleanup.
- It is important in use cases that require a subscription to external data. It is important to clean up so that we don't introduce a memory leak. 
- In React class, a subscription is set up in `componentDidMount` and cleaned up in `componentWillUnmount`. 
- useEffect is designed to keep adding and removing a subscription together. If your effect returns a function, React will run it when it is time to clean up. 
- React performs the cleanup when the component unmounts, this effect runs for every render. 

```js
import React, { useEffect } from 'react'
useEffect(() => {
  // contains first argument which is callback function
  // function will be called after every render, when any piece of state is updated
  console.log('hi, this happens with every render');

  return (() => {
    console.log('this happens with unmount');
  });
});
```

```js
import React, { useEffect } from 'react'
useEffect(() => {
  // runs only on componentDidMount
  // includes empty dependency array 
}, []);
```

```js
import React, { useEffect, useState } from 'react'

const [counter, setCounter] = useState(0);

useEffect(() => {
  // runs on componentDidMount and when counter is updated, when a specific state is updated
  console.log(counter);
}, [counter]);
```