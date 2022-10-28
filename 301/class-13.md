## Readings: More CRUD
---
- POST: Create, GET: Read, PUT: Update, and DELETE. 
1. Which HTTP method would you use to update a record through an API?
- POST: stores requested data sent to our API to our database.
- GET: view stored data, without making any changes or other effects. 
- PUT: updates specified data with new inputs when id is used. 
- DELETE: deletes selected data with target id. 

2. Which REST methods require an ID parameter?
- PUT and DELETE in order to update or delete specified data by id. 

## Speed Coding: Building a CRUD API

1. What’s the relationship between REST and CRUD?
- CRUD is a way of manipulating info and describing the function of an app. 
- REST is controlling data through HTTP commands. It is a way of creating, modifying, and deleting info for the user. 
- CRUD functions can exist in a REST API, but REST APIs are not limited to CRUD functions. 

2. If you had to describe the process of creating a RESTful API in 5 steps, what would they be?
- POST: is the only RESTful API HTTP method that primarily operates on resource collections. When creating a lower position resource in a collection, applying POST to the parent resource prompts it to create a new resource, associate it with proper hierarchy and return a dedicated URL for later reference. 
- PUT: single-resource equivalent of POST. It updates a resource by replacing its content entiretly. It is the most common way to update resource info. 
- PATCH: another way to update resources, but it only modifies resource content. 
- GET: the most common HTTP method. It returns a representational view of a resource's contents and data. Should be used in read-only mode, which keeps data safe and resource indempotent. You should get the same results, no matter how many times used, unless it is modified by another client. 
- DELETE: when targetting a single resource, that resource is removed entirely. Can be somewhat inconsistent in that the URL for the resource may remain avail, even if the actual resource is absent.

[Back to main page](README.md)
