## Readings: CRUD

### Our reading today is based on Status Codes Based On REST Methods & Build A Rest API. 
---

## Status Codes Based On REST Methods 

1. In your own words, describe what each group of status code represents:

- 100’s = Informational status codes; usually tell client that the header part of request has been received and server will try to comply with transmission demand of client. Like using a different protocol or telling the client that its request will fail before they start sending the body. 

- 200’s = Success codes. Tell client that its request was accepted. In case of asynchronous processing of request (202), this doesn't mean the request was successfully processed, only that it met all validation requirements at time of sending. 

- 300’s = Redirection codes. Tell client that resource they are requesting isn't available at expected location anymore. This can have multiple reasons, be temp or perm, but client has to issue a request to new location. 

- 400’s = Client error code. All about invalid requests a client sent to server. Several causes to this, timeouts, wrong URL, missing authen, etc. Client sending incorrect input and should confirm input params are correct before retrying request. 

- 500’s = Server error codes. Often indicate problems with overwhelmed servers or unreachable servers behind proxies. These errors can be temp or perm. 

2. What is a status code 202?
- **Accepted**. Often used for **asynchronous** processing. Code tells client that request was valid, but its processing will finish sometime in future. 
- Response body should include URL to finished resource with some info about when it will be avail, or a URL to some monitoring endpoint that tells client when resource is avail. 

3. What is a status code 308?
- **Permanent Redirect**. Tells client to use another URL to access resource and not use current URL anymore. Helpful when we have multiple endpoints for one resource, but don't want to implement reading from all of them. 

4. What code would you use if an update didn’t return data to a client?
- 204: No Content. Proper code for updates that don't return data to client, for ex. when just saving currently edited document. 

5. What code would you use if a resource used to exist but no longer does?
- 410: Gone. Like 404 but we know resource existed in past, but got deleted or somehow moved, and we don't know where. 

6. What is the ‘Forbidden’ status code?
- 403: Forbidden. Client has authorized or doesn't need to authorize itself, but still has no permissions to access resource. 

## Build A REST API 
- Rest Client is a great extension in VSC where you can test your Rest API. Will need to create a path by naming a file and ending it by .rest or .http.
- In the file, write GET http://localhost:3001/endpoint. This will request the route - send request. 
- To separate two different requests, use ###.

1. Why do we need to pull our MongoDB database string out of our server and put it into our .env?
- When we connect to the database, we will want to use something different than our mongodb localhost. 

2. What is middleware?

3. What does `app.use(express.json())` do?
- Code that runs when the server gets a request but before it gets passed to your routes. 
- Lets our server accept JSON as a body instead of a POST element, GET element, etc. 
 
4. What does the `/:id` mean in a route?
- This is used when you are trying to access specific data that has a unique identifier. 
- req.params.id - id is a param. 

5. What is the difference between `PUT` and `PATCH`?
- PATCH, only updates data with the info that the user passes. 
- PUT, would update all the info of your route all at once, instead of only the info that gets passed. 

6. How do you make a default value in a schema?
- default: Date.now. If a date is not passed, then it will default to current date. 

7. What does a 500 error status code mean?
- Error on the server side which caused the transaction not to work. 

8. What is the difference between a status 200 and a status 201?
- 200: default status, if nothing is sent. Means everything was successful. 
- 201: successfully created an object - more specific. 

[Back to main page](README.md)
