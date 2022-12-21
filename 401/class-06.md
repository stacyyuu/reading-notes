## Authentication

### Securing Passwords
- Store important data like a collection of user data and passwords using a hashing algorithm.
- Cryptographic hash algorithms: MD5, SHA1, SHA256, SHA512, SHA-3.
- They are general purpose hash functions, designed to store huge amounts of data in as short time as possible. 
1. Explain to a non-technical friend how you would safely hash and store a password.
- Hashing allows passwords to be stored in a format that can't be reversed at any reasonable amount of time or cost for a hacker. 
- Hashing algorithms turn plaintext password into an output of characters of a fixed length. It will look nothing like the password. 

2. What is Bcrypt?
- An algorithm that uses a technique called Key Stretching. It makes the brute force attacks slower and minimizes impact.
- It is an adaptive hash function based on the Blowfish symmetric block cipher cryptographic algorithm and introduces a work factor (security factor) which allows you to determine how expensive the hash function ill be. 

3. Why might you use something like Bcrypt?
- The work factor value determines how slow the hash function will be, means different work factor will generate different hash values in different time span. This makes it extremely resistant to brute force attacks. 

### Basic Auth 
1. What is Basic Authentication?
- A method for an HTTP user agent (web browser) to provide a user name and password when making a request. 

2. What properties are necessary in the header of a Basic Auth request?
- Authorization: Basic `<credentials>`

3. How are username:password in Basic Auth encoded?
- Credentials is the Base64 encoding of ID and password joined by a single colon. 

### OWASP Auth Cheat Sheet
1. Define the authentication process to a non-technical recruiter.
- Process of verifying that an individual is who it claims to be. 
- It is commonly performed by submitting a username or ID and one or more items of private information that only a given user should know. 

2. How should your error messaging respond (both HTTP and HTML)? Why?
- An application should respond in a generic manner. 
- This is to prevent the creation of a discrepancy factor, allowing an attacker to mount a user enumeration action against the application. 

3. Bookmark this link also and consider OWASP fundamentals any time you interact with authentication. Applications developed with security in mind from inception have fewer vulnerabilities throughout their lifecycle.
- [Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html)