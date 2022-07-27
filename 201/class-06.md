## JS Object Literals, the DOM

### 7/22/22: Our reading today is based on Problem Domain, Objets, and the DOM. 

---

## JavaScript Object Basics

1. How would you describe an object to a non-technical friend you grew up with?
- An **object** is a standalone entity, with properties, and type. Object properties are basicallty the same as JS variables, except for the attachment to objects. The properties of an object define the characteristics of the object. Objects can also have methods. 
2. What are some advantages to creating object literals?
- An object literal is a comma-separated list of name-value pairs inside of curly braces. These values can be properties and functions. 
- Advantages include convenience, flexibility in declaration, and less code during declaration. You can drop an object literal anywhere in your program with no previous setup and it'll work. 
3. How do objects differ from arrays?
- Objects are used to represent a "thing" in your code. That could be a person, car, building, book, character in a game - basically anything that is made up or can be defined by a set of characteristics. In objects, these characteristics are called properties and consist of key and value. 
- Arrays are used when we want to create and store a list of multiple items in a single variable. Especially useful when creating ordered collections where items in the collection can be accessed by their numerical position in the list. 
4. Give an example for when you would need to use bracket notation to access an object’s property instead of dot notation.
- Dot notation is used mostly as it is easier to read and comprehend and has less verbose. `obj.cat;`
-  When working with bracket notation, property identifiers only have to be a string. They can include any characters, including spaces. Variables may be used as long as the variable resolves to a string. `obj['cat'];`
5. Evaluate the code below. What does the term this refer to and what is the advantage to using this?
- `const dog = {` <br>
  `name: 'Spot',` <br>
  `age: 2,` <br>
  `color: 'white with black spots',` <br>
  `humanAge: function (){`<br>
    `console.log(`${this.name} is ${this.age*7} in human years`);`<br>
  `}`<br>
`}`
- `this` refers to the current object the code is being written inside. If you create more than one object literal, `this` enables you to use the same method definition for every object you create. 

## Introduction to the DOM

1. What is the DOM?
- When a web page is loaded, the browser creates a Document Object Model of the page. 
- The HTML DOM model is constructed as a tree of objects. 
2. Briefly describe the relationship between the DOM and JavaScript.
- With the object model, JavaScript gets all the power it needs to create dynamic HTML:
    - JavaScript can change all the HTML elements in the page
    - JavaScript can change all the HTML attributes in the page
    - JavaScript can change all the CSS styles in the page
    - JavaScript can remove existing HTML elements and attributes
    - JavaScript can add new HTML elements and attributes
    - JavaScript can react to all existing HTML events in the page
    - JavaScript can create new HTML events in the page


[Back to main page](README.md)