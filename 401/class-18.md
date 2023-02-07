## AWS: API, Dynamo, Lambda 

### AWS API Gateway Overview
1. What is Amazon API Gateway?
- Managed service that allows developers to define the HTTP endpoints of a REST API or a WebSocket API and connect those endpoints with the corresponding backend logic. 
- It also handles authentication, access control, monitoring, and tracing of API requests. 

2. Why is Amazon API Gateway an important part of the Serverless ecosystem?
- It conveniently replaces the API servers with a managed serverless solution. 
- It is able to trigger the execution of a Serverless function directly in response to an HTTP request. 
- When using API Gateway together with other AWS services, it's possible to build a fully functional web application without maintaining a server yourself. 

3. How does API Gateway integrate with other AWS services?
- API Gateway integrates with many other AWS services like Lambda, SNS, IAM, and Cognito Identity Pools. 
- These integrations allow for fully managed authentication and authorization layers, as well as detailed metrics and tracing for API requests. 

### AWS API Gateway
1. What are the some benefits of using Amazon API Gateway?
- Supports containerized and serverless workloads, as well as web applications. 

2. What two API types might you choose from?
- RESTful APIs optimized for serverless workloads
- WebSocket APIs, such as chat apps and streaming dashboards

### AWS DynamoDB Guide
1. What is DynamoDB?
- A hosted NoSQL databased offered by AWS.
- It offers reliable performance even as it scales, a managed experience, and a small, simple API. 

2. Under what circumstances would you recommend DynamoDB over MongoDB?
- If you want a fully managed database, meaning that AWS will manage all the scaling, availability, and updates. 

### AWS DynamoDB
1. Explain to a non-technical friend how DynamoDB works.
- It is a key-value NoSQL database that is fully managed by AWS and does not require a server. It can run high-performance applications at any scale. 

### Dynamoose
1. What is Dynamoose?
- A modeling tool for DynamoDB. Heavily inspired by Mongoose. 

2. What are some key features of Dynamoose?
- High level API
- Easy to use syntax
- Strict data modeling 
- Callback & Promise support
