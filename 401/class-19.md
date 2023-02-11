## AWS: Events

### AWS SQS vs SNS
1. What is the difference between SQS and SNS?
- Both are important components for distributed, scalable, and large cloud-based apps. 
- **SQS**: Simple Queue Service. 
- Queueing service for message processing. 
- Recipients have to *poll* SQS to receieve messages. 
- Messages can be stored for a short duration of time (14 days max).
- Can't be received by multiple receivers at the same time. 
- Polling can cause latency in message delivery, unlike SNS where messages are immediately pushed. 
- **SNS**: Simple Notification Service 
- A distributed publish-subscribing service. When publishers send messages to SNS that gets pushed to the subscribers. 
- Sends individual messages or bulk to large numbers of recipients. 
- Fully managed *push* notification service. 
- Notifications can be sent to cell phones, emails, or other services.

2. What are some use cases for both SNS and SQS?
- **SQS use case**: only one subscrible is needed and you only need a simple queue. 
- "Does your system care about an event?"
- **SNS use cases**: multiple subscribers needed and would like to push a bulk of messages. 
- "Do other systems care about an event?"

### AWS SNS & SQS
1. Describe how to use SQS and SNS in a “fanout” pattern.
- **SNS** publishes messages that can be delivered to many subscribers of different types (SQS, Lambda, Email), which is a fan out approach. 
2. Explain how “push notifications” work, using SNS.
- Creating an SNS topic to push out messages through a platform where recipients can subscribe by sending a request with the device's token. 

### SQS & SNS Basics
1. How might a large scale, distributed application make use of a Queue system like SQS?
- It is used by many AWS customers as a building block for building highly reliable and scalable distributed systems. 