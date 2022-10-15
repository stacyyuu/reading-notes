## Readings: Functional Programming 

### Our reading today is based on Functional Programming Concepts and Node JS Tutorials for Beginners. 
---

## Functional Programming Concepts 

1. What is functional programming?
- A programming paradigm - a style of building the structure and elements of computer programs - that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data. 

2. What is a pure function and how do we know if something is a pure function?
- The first fundamental concept that we learn when we want to understand functional programming is **pure functions**. 
- Purity : returns the same result if given the same arguments (it is also referred as deterministic).
- It does not cause any observable side effects. 

3. What are the benefits of a pure function?
- The code is easier to test. There does not have to be anything mocked. 
- They can be tested with different contexts. 

4. What is immutability?
- When data is immutable, its state cannot change after it's created. 
- If you want to change an immutable object, you can't. You have to create a new object with a new value. 

5. What is Referential transparency?
- If a function consistently yields the same results for the same input. 

## Node.JS Tutorial for Beginners - Modules and require()

1. What is a module?
- In Node.JS, our code is split up into logical modules - a different module would be used for a different bit a code, which has a certain functionality in our app. 
- Those modules are called upon whenever they are needed. 
- For instance, you can create a counter module that would be called upon whenever something needed to be counted. 
- A module is essentially another JS file. 

2. What does the word ‘require’ do?
- It is a global function in node which can be used in any file. It basically imports another file into your current file. 
- To create a pathway to another file, you would use require(''), with a string that references that file. 
- require('./'), . means file in current directory. require('./count'), .js is not needed because it automatically finds that file JS. 

3. How do we bring another module into the file the we are working in?

4. What do we have to do to make a module available?
- You must explicitly say which part of the module you want to be available to other files. 
- module.exports = whatever you want to be availble outside of this module (variable names, function names, etc.).
- Then you must create a variable with the same name of the data that the module is requiring from. 

[Back to main page](README.md)
