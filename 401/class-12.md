## Socket.io

### Web Sockets 
1. What is a Web Socket?
- A bidirectional, full-duplex communication protocol used in client-server communication. 
- Unlike HTTP, it starts from ws:// or wss://.
- It is a stateful protocol, which means the connection between client and server will keep alive until terminated by either party. 

2. Describe the Web Socket request/response handshake and what happens once the connection is established.
- To establish a Web Socket connection, the client sends a Web Socket handshake request, for which the server returns a Web Socket handsake response. 
- The handshake starts with an HTTP request/response, allowing servers to handle the HTTP connections as well as Web Socket connections on the same port. 
- Once the connection is established, communication switches to bidirectional binary protocol which does not conform to the HTTP protocol. 

3. Web Sockets provide a standardized way for the server to send content to a client without first receiving a request from that client.

### Socket.io Tutorial
1. What does the event handler io.on() do?
- Adds the listener function to the end of event named eventName (server).
- io.on(eventName, listener)

2. Describe some possible proof of life or proof that the code works as expected.

3. What does socket.emit() do?
- Create and fire custom events. 
- Allows you to emit events on one side and register listeners on the other.

### Socket.io vs Web Sockets
1. What is the difference between WebSocket and Socket.IO? (think Git and GitHub, or OAuth and Auth0).
- Web Socket: communication protocol that provides bidirectional communication between client and server.
- Socket.IO: library that enables real-time and full-duplex communication between client and web servers. 
Client-side: library that runs inside browser
Server-side: library for Node.js

2. When would you use Socket.IO?
- Broadcasting to multiple sockets at a time, it handles the connection transparently. 
- Works on all platforms, server or device, ensuring equality, reliability, and speed. 
- Automatically upgrades the requirement to Web Socket if needed. 

3. When would you use WebSockets?
- Makes real-time communication effortless and efficient. 
- Full-duplex communication, continuous connection with client and server.

### OSI Model Explained 
1. What are a couple of key takeaways from this video?
- OSI Model (Open Systems Interconnection Model) is a conceptual framework used to describe the functions of a networking system. 
- Characterizes computing functions into a universal set of rules and requirements in order to support interoperability between different products and software. 
- Split into seven different layers.
- Physical Layer: lowest layer, concerned with electrically or optically transmitting raw unstructured data bits across the network from the physical layer of the sending device to the physical layer of the receiving device. 
- Data Link Layer: directly connected nodes are used to perform node-to-node data transfer where data is packaged into frames.
- Network Layer: reponsible for receiving frames from the data link layer, and delivering them to their intended destinations based on the addresses contained inside the frame.
- Transport Layer: manages the delivery and error checking of data packets.
- Session layer: controls the conversations between different computers.
- Presentation: formats or translates data for the application layer based on the syntax or semantics that the application accepts. 
- Application Layer: both the end user and the app layer interact directly with the software application. 

### TCP Handshakes Explained
1. Translate the gist of this video to a non-technical friend
- TCP stands for Transmission Control Protocol
- Reliable and connection-oriented transport protocol. Allows data to be delivered succesfully and accurately. 
- Many apps, such as web and email use TCP. 
- Before TCP sends data, it uses a three-way handshake to establish a connection. 

1. Client sends SYN segment to server, asking for sync (the connection). 'Hello server, can you open the connection for me?'
2. Server replies iwth SYN-ACK (sync and acknowledgement). The server acknowledges the client's connection request and also asks the client to open the connection. 
3. Client replies with ACK, which is a 'yes'.
4. Two-way connection is established. 