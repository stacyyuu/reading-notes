## AWS Cloud Servers

### AWS EC2
- Amazon Elastic Compute Cloud. 
- Amazon EC2: Secure and resizable compute capacity for virtually any workload. 
1. What is an EC2 Instance?
- Virtual computing environments. 
- Amazon EC2 offers over 500 instances optimized to fit different use cases. 
- Instance types comprise varying combos of CPU, memory, storage, and networking capacity and give you flexibility to choose the appropriate mix of resources for your app. 
- General purpose instances provide a balance of compute, memory and networking resources. It can be used for a variety of diverse workloads. 
- Compute optimized instances are ideal for compute bound apps that benefit from high performance processes. 
- Memory optimized instances are designed to deliver fast performance for workloads that process large data sets in memory. 
2. Name 2 use cases for EC2.
- Run cloud-native and enterprise apps
- Develop for Apple platforms
3. Provide 1 reason to use ECS instead of a service such as Heroku, Digital Ocean, or Render.com.
- EC2 eliminates the need to invest in hardwore up front, so you can develop and deploy apps faster. 
- It can be used to launch as many or as few virtual servers as you need. 

### EC2 For Humans
1. Where can we find EC2 on the AWS Console?
- Under the computer services 
2. Explain the general difference between T2 Micro and XL.
- T2 instances are a low-cost, general purpose instance type that provides a baseline of CPU performance with the ability to burst above when needed. 
- T2 micro: 1 vCPUs, 1.0 RAM (GiB), 6 CPU Credits/hr
- T2 XL: 4 vCPUs, 16.0 RAM (GiB), 54 CPU Credits/hr
3. Explain a “Compute Cycle” to a non-technical friend.
- Fetch - retrieve instruction from memory
- Decode - translate the retrieved instruction into computer commands
- Execute - execute the computer commands
- Store - send and write results back in memory 

### EC2 For Humans 
1. What is Elastic Beanstalk?
- Easy to use service that deploys, manages, and scales web apps and services for you. 
2. Describe the relationship between EC2 and Elastic Beanstalk.
- Elastic Beanstalk leverages EC2. It supports serveral Amazon EC2 instance purchasing options. 
3. Name some benefits of using Elastic Beanstalk.
- Auto scales your app based on easy auto scale settings. 
- Monitors the health of your app. 
- Decreases time in managing and configuring infrastructures. 