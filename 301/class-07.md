## Readings: REST

### Our reading today is based on What Google Learned From Its Quest to Build the Perfect Team, REST, and Requesting API Keys.
---

## How I explained REST to my brother 
1. Who is Roy Fielding?
- Helped write the first web servers that sent documents across the internet.
- He did a ton of research explaining why the web works the way it does. 
- His name is on specification for the protocol that is used to get pages from servers to your browser. 
- The protocol is HTTP. 
- Protocol is about applying verbs to nouns. 
- Browser does HTTP GET on the URL typed in and a webpage comes back. 

2. Why don’t the techniques that we use today work well when we need to be able to talk to all of the machines in the world?
- They weren't designed to be used like that.
- Most of the techniques developed later were used to get computers to talk to each other and didn't have those requirements. They just needed to talk to a small group of machines. 
- We need to be able to talk to all machines about all the stuff that's on all the other machines. So we need some way of having one machine tell another machine about a resource that might be on yet another machine. 
- Machines tell each other where things are with a URL. 
- Every programming language, database, or other kind of system has a different way of talking about nouns. There is no universal noun. 
- That's why URL is so important. It lets all of these systems tell each other about each other's nouns. 
- There's a powerful concept in programming and CS theory called 'polymorphism'. Different nouns can have the same verb applied to them.

3. What is the HTTP protocol that Fielding and his friends created?
- The first part tells the browser what protocol to use. What is typed in there is one of the most important breakthroughs in the history of computing. 
- It is capable of describing the location of something anywhere in the world from anywhere in the world. It's the foundation of the web.
- The whole world wide web is built on an architectural style called 'Rest'. REST provides a definition of 'resource', which is what those things point to. 
- A web page is a 'representation' of a resource. Resources are just concepts. URLS- those things you type into the browser. 
- The URL tells the browser there's a concept somwehere. 
- A browser can then ask for a specific representation of the concept. Specifically, the browser asks for the web page representation of the concept. 
- GET, PUT, DELETE are universal and can be applied to different nouns. 

4. What does a `GET` do?
- GETs a resource. On machines, it will ask for machine-readable. On browser, it will ask for human-readable 'representation' of that data. 

5. What does a `POST` do?
- Used when a system needs to add something to another system. 

6. What does `PUT` do?
- Used when a system wants to replace something in another system.

7. What does `PATCH` do?
- Used when a system wants to partially update something in another system. 

[Back to main page](README.md)