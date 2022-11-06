## Readings: Authentication
---

## OAuth
1. What is OAuth?
- Open-standard authorization protocol or framework that describes how unrelated servers and services can safely allow authenticated access to their assets without actually sharing the initial, related, single logon credential. 
- In authentication parlance, this is known as secure, third-party, user-agent, delegated authorization. 

2. Give an example of what using OAuth would look like.
- When you log onto a website and it offers one or more opportunities to log on using another website's/service's logon. 
- You then click on the button linked to the other website, the other website authenticates you, and the website you were originally connecting to logs you on itself afterward using permission gained from the second website. 
- When creating an account and connecting through gmail, facebook, github, paypal, etc. 

3. How does OAuth work? What are the steps that it takes to authenticate the user?
- First website connects to second on behalf of the user, using OAuth, providing the user's verified identity. 
- Second site generates one-time token and one-time secret unique to the transaction and parties involved. 
- First site gives token and secret to the initiating user's client software. 
- Client's software presents request token and secret to their authorization provider (which may or may not be the second site).
- If not already authenticated to authorization provider, the client may be asked to authenticate. After authentication, the client is asked to approve the authorization transaction to the second website. 
- User approves (or their software silently approves) a particular transaction type at the first website.
- User is given an approved access token (notice it's no longer a request token).
- User gives approved access token to first website. 
- First website gives access token to second as proof of authentication on behalf of user.
- Second website lets first access their site on behalf of user. 
- User sees a successfully completed transaction occurring. 
- What is special about OAuth is its ability to work across the web and its wide adoption. 

4. What is OpenID?
- OpenID is used for authentication, not authorization. 
- "OpenID is for humans logging into machines, OAuth is for machines logging into machines on behalf of humans."

## Authorization and Authentication Flows
1. The difference between authorization and authentication:

|Authentication |  Authorization |
| :---: | :---: |
|Determines whether users are who they claim to be |	Determines what users can and cannot access |
| Challenges the user to validate credentials (for example, through passwords, answers to security questions, or facial recognition) |	Verifies whether access is allowed through policies and rules |
| Usually done before authorization  | Usually done after successful authentication |
| Generally, transmits info through an ID Token	 | Generally, transmits info through an Access Token |
| Generally governed by the OpenID Connect (OIDC) protocol |	Generally governed by the OAuth 2.0 framework |
| Example: Employees in a company are required to authenticate through the network before accessing their company email |	Example: After an employee successfully authenticates, the system determines what information the employees are allowed to access |

2. What is Authorization Code Flow?
- Because regular web apps are server-side apps where the source code is not publicly exposed, they can use the Authorization Code Flow, which exchanges an Authorization Code for a token. 
- Your app must be server-side because during this exchange, you must also pass along your 

3. What is Authorization Code Flow with Proof Key for Code Exchange (PKCE)?
- PKCE-enhanced Authorization Code Flow introduces a secret created by the calling app that can be verified by the authorization server; this secret is called the Code Verifier. 
- Additionally, the calling app creates a transform value of the Code Verifier called the Code Challenge and sends this value over HTTPS to retrieve an Authorization Code. 
- This way, a malicious attacker can only intercept the Authorization Code, and they cannot exchange it for a token without the Code Verifier. 

4. What is Implicit Flow with Form Post?
- Implicit Flow with Form Post flow uses OIDC (OpenID Connect) to implement web sign-in that is very similar to the way SAML and WS-Federation operates. 
- The web app requests and obtains tokens through the front channel, without the need for secrets or extra backend calls. 
- With this method, you don't need to obtain, maintain, use, and protect a secret in your app. 

5. What is Client Credentials Flow?
- The client can request an access token using only its client credentials (or other supported means of authentication) when the client is requesting access to the protected resources under its control, or those of another resource owner that have been previously arranged with the authorization server (the method of which is beyond the scope of this specification).

6. What is Device Authorization Flow?
- The 0Auth 2.0 device authorization grant is designed for Internet-connected devices that either lack a browser to perform a user-agent-based authorization or are input constrained to the extent that requiring the user to input text in order to authenticate during the authorization flow is impractical. 
- It enables 0Auth clients on such devices (like smart TVs, media consoles, digital picture frames, and printers) to obtain user authorization to access protected resources by using a user agent on a separate device. 

7. What is Resource Owner Password Flow?
- The resource owner password credentials grant type is suitable in cases where the resource owner has a trusted relationship with the client, such as the device operating system or a highly privileged app. 
- The authorization server should take special care when enabling this grant type and only allow it when other flows are not viable. 
- This grant type is suitable for clients capable of obtaining the resource owner's credentials (username and password, typically using an interactive form).
- It is also used to migrate existing clients using direct authentication schemes such as HTTP Basic or Digest authentication to 0Auth by converting the stored credentials to an access token. 

[Back to main page](README.md)
