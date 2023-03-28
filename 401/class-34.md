# API Integration

### API Server Build
1. Explain the difference between a query string parameter and a path parameter.
- Path parameter allows you to access the path where you are looking for data
- `/products`
- Query string parameter allows you to filter for a specific category in that path 
- `/products?category=electronics`

2. What would our API URL with a path id parameter be given the following information: `http://our-site.com/v3/stuff/things`
    - Domain: `http://our-site.com`
    - `v3`
    - model name: `stuff`
    - id: `things`

3. We have created a dynamic API with an “interface”. Describe how that interface works to a non-technical friend.
- An interface is a point where two things meet and interact.
- For our webpage, we will be using a user interface in order to request and receive data from our API.

### Auth Server Build
1. Describe how you would use middleware to implement basic and bearer auth.
- Middleware is used for handling 404 and 500 conditions.
- It is also used for handling each type of authentication. 
- Basic (username + password) to be used on /login route.
- Bearer (token) to be used on an other route in the server that requires a logged in user.
- It should run after Bearer Middleware on routes to be protected.
- It accepts 'capability' as a parameter.

2. Describe the handshake necessary to implement OAuth.
- It is initiated in the browser, using a 3rd party authentication/authorization service. Once the user has granted permission, it will invoke a GET on the `/oauth` route. The OAuth middleware should complete the handshaking process at this point. 
- It will create/update a local user account in the database and return an object with a re-authentication/bearer token and the user object. 


3. Describe how Role Based Access Control works to a non-technical friend.
- User roles are pre-defined and will have a list of allowed capabilities that allow them to read, create, update, or delete in our app. 