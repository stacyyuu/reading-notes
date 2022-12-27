## Bearer Authorization

### Intro to JWT

1. What is a JSON Web Token (JWT)?
- Open, industry standard (anyone can use it) RFC 7519 method for representing claims securely between two parties. 
- Information is transmitted as a JSON object. 
- This information can be verified and trusted because it is digitally signed. 
- It can be signed using a secret (HMAC algorithm) or a public/private key pair using RDA or ECDSA. 

2. When should we use JSON Web Tokens?

- **Authorization**: Most common. Once the user is logged in, each request will include the JWT, allowing the user to access other services and routes that are permitted. 
- Whenever the user wants access to a protected route or service, the user agent sends the JWT, typically in the **Authorization** header using the **Bearer** schema. 
- `Authorization: Bearer <token>`
- **Information Exchange**: JWT are a good way of securely transmitting information between parties. 

3. Claims are expected in which structural component of a JWT?
- Appears in key/value pairs where the name is always a string and the value can be any JSON value. It is contained in a JSON object. 

### Are JWTs Secure?
1. If I get a JWT and I can decode the payload, how can we call that secure?
- JWTs can be either signed, encrypted, or both. If a token is signed, but not encrypted, everyone can read its contents, but when you don't know the private key, you can't change it. Otherwise, the receiver will notice that the signature won't match anymore. 

2. If sending a JWT, what must sender and receiver both know? Hint, it’s appended in the signature.
- The sender and receiver will both need to know the secret in order to confirm the signature. 
- If someone attempts to change something, they won't know the secret and the signature would no longer match. 

3. Explain how concatenated content and secret can be sent and received securely to a non-technical recruiter.
- Content + secret can be sent using a Hash function. The signature will turn into a hashed signature that is calculated using the content + secret. The same calculated signature can not be replicated unless the exact secret is used. 

### JWTs Explained
1. Why use JWT?
- It is digitally signed, information is verified and trusted. 
- Useful for Authentication and Information Exchange between two bodies. 

2. JWT is Compact and self-contained. Describe how this is useful to a non-technical friend.
- It can send it through URL as a get request, then you can send as a POST request in the HTTP header. 
- This allows fast transmission. 
- It contains all the information of the user in the token. 
- It avoids querying the database more than once. The user will only have to log in once and be able to access other parts of the webpage using the token. 

3. What are the three components (the structure) of a JWT signature?
- Header: JSON object, contains alg (which algorithm it is encoded with) and typ (type of JWT token). This is Base64URL encoded to form the first part. 
- Payload: JSON object, contains the claims aka user details or additional metadata (expiry date of token). This is Base64 URL encoded to form the second part. 
- Signature: Most important. Ensures that the content is not changed when passed. 
- Uses base64 header concatenated with base64 payload and secret. This is encoded with an algorithm. 