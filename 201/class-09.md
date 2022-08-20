## Forms and JS Events

### Our reading today is based on HTML forms and introduction to events in JS. 
---

## HTML Forms: First Web Form & How to Structure it

1. Why are forms so important in web development?
- **Web forms** are one of the main points of interaction between a user and a web site or application. 
- Forms allow users to enter data, which is generally sent to a web server for processing and storage, or used on the client-side to immediately update the interface in some way. 
- A web form's HTML is made up of one or more **form controls** (sometimes called **widgets**), plus some additional elements to help structure the overall form - they are often referred to as **HTML forms**.
- Ex. Text fields, checkboxes, radio buttons, submit buttons, etc. 

2. When designing a form, what are some key things to keep in mind when it comes to user experience?
- Before starting to code, it's always better to step back and take the time to think about your form. Designing a quick mockup will help you define the right set of data you want to ask your user to enter. 
- From a UX POV, it's important to remember that the bigger your form, the more you risk frustrating people and losing users. Keep it simple and stay focused: ask only for the data you absolutely need. 

3. List 5 form elements and explain their importance.
- `<form>`: To define a HTML form for user inputs 
- `<input>`: To definte input control 
- `<datalist>`: To specify a list of pre-dfined options
- `<fieldset>`: To define group related elements
- `<label>`: To define a label of input
- `<legend>`: To define a captaion for fieldset


## Learn JS: Introduction to Events

1. How would you describe events to a non-technical friend?
- Events are actions or occurrences that happen in the system you are programming - the system produces a signal of some kind when an event occurs, and provides a mechanism by which an action can be automatically taken when the event occurs. 
- Ex. If user clicks a button on webpage, you might want to react to that action by displaying an information box. 
- Ex. In airport, when the runway is clear for take off, a signal is communicated to the pilot. As a result, the plane can safely take off. 

2. When using the `addEventListener()` method, what 2 arguments will you need to provide?
- Objects that can fire events have an `addEventListener()` method, that takes at least two arguments: the name of the event and a function to handle the event. 

3. Describe the event object. Why is the target within the event object useful?
- Sometimes, inside an event handler function, you'll see a parameter specified with a name such as `event`, `evt`, or `e`. This is called the **event object**, and it is automatically passed to event handlers to provide extra features and information. 
- The `target` property of the event object is always a reference to the element the event occured upon. 

4. What is the difference between event bubbling and event capturing?
- **Event bubbling** and **capture** are terms that describe phases in how the browser handles events targeted at nested elements. 
- **In the capturing phase:**
- The browser checks to see if the element's outer-most ancestor (`<html>`) has a `click` event handler registered on it for the capturing phase, and runs it if so.
Then it moves on to the next element inside `<html>` and does the same thing, then the next one, and so on until it reaches the direct parent of the element that was actually clicked.
- **In the target phase:**
- The browser checks to see if the `target` property has an event handler for the `click` event registered on it, and runs it if so.
Then, if `bubbles` is `true`, it propagates the event to the direct parent of the clicked element, then the next one, and so on until it reaches the `<html>` element. Otherwise, if `bubbles` is `false`, it doesn't propagate the event to any ancestors of the target.
- **In the bubbling phase, the exact opposite of the capturing phase occurs:**
- The browser checks to see if the direct parent of the clicked element has a `click` event handler registered on it for the bubbling phase, and runs it if so.
Then it moves on to the next immediate ancestor element and does the same thing, then the next one, and so on until it reaches the `<html>` element.


[Back to main page](README.md)