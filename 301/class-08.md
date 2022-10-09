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

4. What are the most common HTTP verbs?
- **GET** : retrieves representation of the resource at the specified URI. 
- The body of response message contains the details of the requested resource.
- **POST** : creates a new resource at the specified URI. The body of the request message provides the details of the new resource. Note that POST can also be used to trigger operations that don't actually create resources. 
- **PUT** : either creates or replaces the resource at the specified URI. The body of the request message specifies the resource to be created or updated. 
- **PATCH** : preforms a partial update of a resource. The request body specifies the set of changes to apply to the resource.
- **DELETE** : removes the resource at the specified URI.

5. What should the URIs be based on?
- Resource URIs should be based on nouns (the resource) not the verbs (the operations on resources).

6. Give an example of a good URI.
- HTTP
https://adventure-works.com/orders // Good
https://adventure-works.com/create-order // Avoid

7. What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?
- All web requests impose a load on the web server. The more requests, the bigger the load. 
- Therefore, try to avoid 'chatty' web APIs that expose a large number of small resources. 
- This kind of API may require a client app to send multiple requests to find all of the data it requires. 
- Instead, you may want to denormalize data and combine related info into bigger resources that can be retrieved with a single request. 

8. What status code does a successful `GET` request return?
- A successful GET method typically returns HTTP status code 200 (OK). If the resource cannot be found, the method should return 404 (Not Found).

9. What status code does an unsuccessful `GET` request return?
- If POST creates a new resource, it returns HTTP status code 201 (Created). The URI of the new resource is included in the Location header of the response. The response body contains a representation of the resource. 
- If method does some processing but does not create a new resource, the method can return HTTP status code 200 and include the result of operation in the response body. 
- If there is no result to return, the method can return HTTP status code 204 (No Content) with no response body. 

10. What status code does a successful `POST` request return?
- If a PUT method creates a new resource, it returns HTTP status code 201 (Created), as with a POST method. If the method updates an existing resource, it returns either 200 (OK) or 204 (No Content). In some cases, it might not be possible to update an existing resource. In that case, consider returning HTTP status code 409 (Conflict).

11. What status code does a successful `DELETE` request return?
- With a PATCH request, the client sends a set of updates to an existing resource, in the form of a patch document. The server processes the patch document to perform the update. The patch document doesn't describe the whole resource, only a set of changes to apply.

[Back to main page](README.md)
