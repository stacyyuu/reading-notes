## HTML Tables, JS Constructor Functions

### 7/29/22 Our reading today is based on Object-Oriented Programming, HTML Tables.

---

## Domain Modeling

1. Explain why we need domain modeling.
- **Domain Modeling** is the process of creating a conceptual model in code for a specific problem. A model describes the various entities, their attributes and behaviors, as well as the constraints that govern the problem domain. An entity that stores data in properties and encapsulates behaviors in methods is commonly referred to as an object-oriented model.
- A domain model that's articulated well can verify and validate the understanding of specific problem among various stakeholders. As a communication tool, it defines a vocabulary that can be used within and between both technical and business teams. 

## HTML Tables Basics

1. Why should tables not be used for page layouts?
- A table is a structured set of data made up of rows and columns (tabular data). A table allows you to quickly and easily look up values that indicate some kind of connection between different types of data, for example a person and their age, or a day of the week, or the timetable for a local swimming pool. 
- Tables should be used for tabular data. Using tables as a page layout is old school and does not look presentable these days.

2. List and describe 3 different semantic HTML elements used in an HTML `<table>`.
- `<header>, <section>, <article>,` or `<div>` are proper layout containers. 


## Introducing Constructors

1. What is a constructor and what are some advantages to using it?
- Using object literals are not efficient when creating more than one object. 
- We would like a way to define the "shape" of an object - the set of methods and the properties it can have - and then create as many objects as wel like, just updating the values for the properties that are different.
- The first version of this is just a function... a function can create and return a new object each time we call it. The object will have two members: a property name and a method introduceSelf().
- `function createPerson(name) {` <br>
  `const obj = {};` <br>
  `obj.name = name;` <br>
  `obj.introduceSelf = function() {` <br>
    `console.log(`Hi! I'm ${this.name}.`);` <br>
  `}` <br>
  `return obj;` <br>
`}` 
- A **constructor** is just a function called using the `new` keyword. When you call a constructor, it will: create a new object, bind `this` to the new object, so you can refer `this` in your constructor code, run the code in the constructor, return the new object. 
- Constructors start with a capital letter and are named for the type of object they create. 

2. How does the term `this` differ when used in an object literal versus when used in a constructor? 
- The `this` keyword refers to the newly created object in a constructor. It becomes the current instance object.

## Object Prototypes Using A Constructor
1. Explain prototypes and inheritance via an analogy from your previous work experience.
NOTE: This is a very common front end developer interview question
- In JavaScript, an object can inherit properties of another object. The object from where the properties are inherited is called the **prototype**. In short, objects can inherit properties from other objects - the prototype.
- Inheritance solves the problem of data and logic duplication. By inheriting, objects can share properties and methods without the need of manually setting those properties and methods on each object. 