## Readings: APIs

### Our reading today is based on API Best Design Practices
---

## API Best Design Practices 

1. What does REST stand for?
- Representational State Transfer. 
- Created by Roy Fielding in 200. It is an architectural approach to designing web services. 
- An architectural style for building distributed systems based on hypermedia. REST is independent of any underlying protocol and is not necessarily tied to HTTP. 
- However, most common REST API implementations use HTTP as the application protocol, and this guide focuses on designing REST APIs for HTTP. 

2. REST APIs are designed around a ____.
- REST APIs are designed around resources, which are any kind of object, data, or service that can be accessed by the client. 
- A resource has an identifier, which is a URL that uniquely identifies that resource. 

3. What is an identifier of a resource? Give an example.
- For example, the URI for a particular customer order might be:
HTTP
https://adventure-works.com/orders/1

6. What are the most common HTTP verbs?
- **GET** : retrieves representation of the resource at the specified URL. 

8. What should the URIs be based on?
9. Give an example of a good URI.
10. What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?
11. What status code does a successful `GET` request return?
12. What status code does an unsuccessful `GET` request return?
13. What status code does a successful `POST` request return?
14. What status code does a successful `DELETE` request return?
