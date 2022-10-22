## Readings: In Memory Storage

### Our reading today is based on Understanding the JavaScript Call Stack and JavaScript Error Messages. 
---

## Understanding the JavaScript Call Stack 

- Call stack is primarily used for function invocation (call). 
- Since the call stack is single, function(s) execution, is done one at a time from top to bottom. 
- It means the call stack is synchronous. 
- A call stack is a data structure that uses the Last In, First Out (LIFO) principle to temporarily store and manage function invocation (call).

1. What is a ‘call’?
- A function invocation. 

2. How many ‘calls’ can happen at once?
- Single. 

3. What does LIFO mean?
- Last In, First Out. 
- It means that the last function that gets pushed into the stack is the first to be popped out when the fucntion returns. 

4. Draw an example of a call stack and the functions that would need to be invoked to generate that call stack.
- `function firstFunction(){`<bR>
  `console.log("Hello from firstFunction");`
`}`
- `function secondFunction(){`<br>
  `firstFunction();`<br>
  `console.log("The end from secondFunction");`
`}` <br>  `secondFunction();`

1. When `secondFunction()` gets executed, an empty stack frame is created. It is the main (anonymous) entry point of the program.
2. `secondFunction()` then calls `firstFunction()` which is pushed into the stack.
3. `firstFunction()` returns and prints “Hello from firstFunction” to the console.
4. `firstFunction()` is popped off the stack.
5. The execution order then moves to `secondFunction()`.
6. `secondFunction()`returns and prints “The end from secondFunction” to the console.
7. `secondFunction()` is popped off the stack, clearing the memory.

5. What causes a Stack Overflow?
- Occurs when there is a recursive function (a function that calls itself) without an exit point. 
- The browser (hosting environment) has a max stack call that it can accomodate before throwing a stack error. 
- `function callMyself(){` <br>
  `callMyself();`<br>
`}`<br>
`callMyself();`

## JavaScript Error Messages 

1. What is a ‘reference error’?
- Using a variable that is not yet declared. 
- When `const` and `let` are hoisted before being declared. This is called Temporal Dead Zone (TDZ).

2. What is a ‘syntax error’?
- Something that cannot be parsed in terms of syntax. 
- Solved by fixing the syntax. 

3. What is a ‘range error’?
- Manipulating an object with some kind of length and giving it an invalid length. 
- Same for arrays. 

4. What is a ‘type error’?
- When the types (numbers, string, so on) you are trying to use or access are incompatible, like accesing a property in an `undefined` type of variable. 
- Most frequent error in JS. 
- Make sure a value exists before trying to access it by either creating it or by checking for `undefined`. 

5. What is a breakpoint?
- In the debugger window, you can set breakpoints in the JS code. 
- At each breakpoint, JS will stop executing, and let you examine the JS values. 
- After examining values, you can resume the execution of code. 

6. What does the word ‘debugger’ do in your code?
- Stops the execution of JS, and calls (if avail) the debugging function. 
- Has the same function as setting a breakpoint in the debugger. 
- If no debugging is avail, the debugger statement has no effect. 

[Back to main page](README.md)
