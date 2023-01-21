## Message Queues

### Socket.io Chat Example

1. Explain to a non-technical recruiter what the Chat Example (above) does.
- Sockets have been useful for real-time chat systems.
- They provide a bidirectional communication channel between a client and server.
- When the server receives messages, it is able to push the message to the client. 
2. What proof of life are we getting on the backend from the above app?
- 'listening on :3000'
3. Socket.IO gives us the i0.emit() method to send an event to everyone. What flag would you use if you want to send a message to everyone except for a certain emitting socket?
- Use the broadcast flag
<br>
`io.on('connection', (socket) => {` <br>
  `socket.broadcast.emit('hi');` <br>
`});`

### Rooms

1. What is a room and how might a room be useful?
- Rooms are channels that sockets can `join` and `leave`. It can be used to broadcast events to a subset of clients. 
2. How do you join a room?
- You can call `join` to subscribe the socket to a given channel. <br>
`io.on("connection", (socket) => {` <br>
  `socket.join("some room");` <br>
`});`
- Then simply use `to` or `in` (they are the same) when broadcasting or emitting. <br>
`io.to("some room").emit("some event");`
- You can also emit to several rooms at a time. 
3. how do you leave a room?
- Upon disconnection, sockets `leave` all channels they were a part of automatically and no special teardown is needed.
- The rooms can be fetched by listening to the `disconnecting` event. 

### Namespaces

1. What is a Namespace and what does it allow you to do?
- A communication channel that allows you to split the logic of your app over a single shared connection. 
- It is also referred to as multiplexing. 
2. Each namespace potentially has its own what? (hint: 3 things)
- event handlers
- rooms
- middlewares: a function that gets executed for every incoming connection - useful for logging, auth, rate limiting.
3. Discuss a possible use case for separate namespaces
- Creating a namespace that only authorized users have access to, so the logic related to those users is separated from the rest of the app.
- Your app has multiple tenants so that you want to dynamically create one namespace per tenant. 