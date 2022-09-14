## Readings: Introduction to React and Components 

### Our reading today is based on component-based architecture and using props. 
---
## Component-Based Architecture

Component-based architecture focuses on the decomposition of the design into individual functional or logical components that represent well-defined communication interfaces containing methods, events, and properties. It provides a higher level of abstraction and divides the problem into sub-problems, each associated with component partitions. 

1. What is a “component”?
- A modular, portable, replaceable, and reusable set of well-defined functionality that encapsulates its implementation and exporting it as a higher-level interface
- A software object, intended to interact with other components, encapsulating certain functionality or a set of functionalities
- A software component can be defined as a unit of composition with a contractually specified interface and explicit context dependencies only. That is, a software component can be deployed independently and is subject to composition by third parties. 


2. What are the characteristics of a component?
- **Reusability**: Components are usually designed to be reused in different situations in different applications. However, some components may be designed for a specific task. 
- **Replaceable**: Components may be freely substituted with other similar components. 
- **Not context specific**: Components are designed to operate in different environments and contexts. 
- **Extensible**: A component can be extended from existing components to provide new behavior. 
- **Encapsulated**: A component depicts the interfaces, which allow the caller to use its functionality, and do not expose details of the internal processes or any internal variables or state. 
- **Independent**: Components are designed to have minimal dependencies on other components. 


3. What are the advantages of using component-based architecture?
- **Ease of deployment**: As new compatible versions become available, it’s easier to replace existing versions with no impact on the other components or system as a whole. 
- **Reduced cost**: Use of third-party components allows you to spread the cost of development and maintenance. 
- **Ease of development**: Components implement well-known interfaces to provide defined functionality, allowing development without impacting other parts of the system. 
- **Reusable**: Use of reusable components means that they can be used to spread the development and maintenance cost across several applications or systems. 
- **Modification of technical complexity**: A component modifies the complexity through use of a component container and its service. 
- **Reliability**: The overall system reliability increases since the reliability of each individual component enhances the reliability of the whole system via reuse. 
- **System maintenance and evolution**: Easy to change and update the implementation without affecting the rest of the system. 
- **Independent**: Independency and flexible connectivity of components. Independent development of components by different groups in parallel. Productivity for software development and future software development. 

## What is Props and How to Use it in React

1. What is “props” short for?
- Props stands for **properties**, which is a special keyword in React. It is used for passing data from one component to another. Similar to function arguments. 
- Data with props are being passed in a **uni-directional flow**. 
- Props data is **read-only** (immutable), which means that data coming from the parent should not be changed by child components. 

2. How are props used in React?
- Firstly, define an attribute and its value (data)
- Then pass it to child component(s) by using Props
- Finally, render the Props Data <br>
`class ParentComponent extends Component { `<br>
 `render () {`<br>
   `return (`<br>
     `<h1>`
       `I'm the parent component.`
       `<ChildComponent />`
     `</h1>`<br>
   `);`
 `}`
`}`

3. What is the flow of props?
- The flow of props is **uni-directional**, meaning the data is passed one way from parent to child. 

[Back to main page](README.md)