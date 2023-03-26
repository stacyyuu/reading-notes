# Login and Auth 

### What is Role Based Access Control (RBAC)
1. What is Role Based Access Control (RBAC)?
- Restricts network access based on a person's role within an organization and has become one of the main methods for advanced access controls. 
- The roles refer to the levels of access that employees have to the network. 
- Employees are only allowed to access the info necessary to effectively perform their job duties. 

2. Share some an example of RBAC including all possible CRUD 
operations and correlating roles.
- Office Manager - CRUD
- Provider - CRU
- Front Desk - CRU
- Patient - R

3. What are the Benefits of RBAC?
- Reducing administrative work and IT support, maximizing operational efficiency, and improving compliance. 

### react-cookie-library and react-cookies component
1. Describe some react-cookie features.
- `<CookiesProvider />` set the user cookies
- `useCookies([dependencies])` access and modify cookies using React hooks
- Dependencies lets you optionally specify a list of cookie names your component depends on or that should trigger a re-render. If unspecified, it will render on every cookie change. 
- `cookies` js object with all your cookies. 
- `setCookie(name, value. [options])` set a cookie value
- `removeCookie(name, [options])`
- `withCookies(Component)` give access to your cookies anywhere

2. Describe some react-cookies features.
- Load and save cookies with React
- To be able to access user cookies while doing server-rending, you can use `plugToRequest` or `setRawCookie`
- `.load(name, [doNotParse])`
- `.loadAll()` load all available cookies
- `.select([regex])` find all cookies with a name that match the regex
- `.save(name, value, [options])` set a cookie


3. Which library would you prefer would you prefer? Why?
- I would prefer to use the react-cookie library because it's similar to the way we have been setting state and using hooks. It seems more clear and easier to understand. 