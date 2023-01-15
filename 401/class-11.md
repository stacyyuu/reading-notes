## Event Driven Applications

### Event Driven Programming 
1. What native Node.js module allows us to get started with Event Driven Programming?
- EventEmitter allows us to get started with Event-Driven Programming in our project right away. 
- Flow of the program is determined by events such as user actions, sensor outputs, or message passing from other programs or threads. 
- Generally a main loop that listens for events and then triggers a callback function. 

2. What is the value of Object Oriented Programming used in tandem with Event Driven Programming?
-OOP approach promotes idea that all behavior of an individual unit (or object) be handled from code within that unit. Apps are built with many different units that all speak to and interact with each other. 
- By registering event listeners we can reverse the flow of communication between our objects. 
- Rather than an object needing to reach inside another object to trigger a function, our objects can just emit events and whichever objects are listening to those events will process it in a way they have been told. 
- The source of an objects behavior is now entirely contained within itself, rather than needing to be accessed by external objects.

3. Consider your knowledge of Event Driven Programming in the Web Browser, now explain to a non-technical friend how Event Driven Programming might be useful on the backend using Node.js.
- It is useful when applications whose control flow are based, not on its structure, but rather on internal or external events. 