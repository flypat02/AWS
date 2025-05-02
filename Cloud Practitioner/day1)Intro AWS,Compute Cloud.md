# Practitioner Essentials 1일차

# Amazon EC2

### on-premises resources

- Spend money upfront to purchse hardware
- Wait for the servers to be delivered to you
- Install the servers in your physical data center
- Make all the necessary configurations

### EC2

- You can provision and launch an Amazon EC2 instance within minutes
- You can using it when you have finished running a workload
- You pay only for compute time you use when an instance is running, not when it is stopped or terminated
- You can sae costs by paying only for server capacity that you need or want

---

## EC2 Instance Types

- General purpose instances
    - Provide a balance of comput, memory, and networking resources
- Compute optimized instances
    - Ideal for compute-bound applications that benefit from high-performance processors
- Memory optimized instances
    - Designed to deliver fast performance for workloads that process large datasets in memory
- Accelerated computing instances
    - Use hardware accelerators, or coprocessors, to perform some functions more efficiently than is possible in software on CPUs
- Storage optimized instances
    - Designed for workloads that require high, sequential read and write access to large datasets on local storage

---

## EC2 pricing

- On-Demand
    - Ideal for short-term, irregualr workloads that cannot be interrupted
- Reserved Instances
    - Billing discount applied to the use of On-Demand Instances in your account
    - There are two available types of Reserved Instances
        
        Reserved Instances
        -This option is a good fit if you know the EC2 instance type and size you need for your steady-state applications and in which AWS Region you plan to run them 
        
        Convertible Reserved Instances
        -If you need to run your EC2 instances in different Availability Zones or different instance types, then Convertible Reserved Instances might be right for you
        
- EC2 Instance Savings Plans
    - Reduce your EC2 instance costs when you make an hourly spend commitment to an instance family and Region for a 1 year or 3 year term
    - Good options if you need flexibility in your EC2 usaged over the duratio fo the commitment term
- Spot Instances
    - Ideal workloads with flexible start and end times, or that can withstand interruptions
    - It use unused EC2 computing capacity and offer you cost savings at up to 90%
- Dedicated Hosts
    - Physical servers with EC2 instance capacity that is fully dedicated to your use
    - Of all EC2 options that were coverd, Dedicated Host are the most expensive

---

## Scaling EC2

### Scalability

- Involves beginning with only the resources you need and designing your architecture to automatially respond to changing demand by sacalig out or in

## EC2 Auto Scaling

- Enables you to automatically add or remove EC2 instances in response to changing application demand
- Dynamic sccaling
    - Responds to changing demand
- Predictive sacling
    - Automatically schedules the right number of EC2 instances based on predicted demand

![](https://explore.skillbuilder.aws/files/a/w/aws_prod1_docebosaas_com/1746086400/EodoxqQXUJd_rFQ8cIsZKQ/tincan/fe470bc5add63f94f005d3da17a6db8131e78b9e/assets/CPE%20Digital%20-%20Auto%20Scaling%20pt%202.png)

Minimum capacity

- The number of EC2 instances that launch immediately after you have created the Auto Scaling group

Desired capacity

- You can set the Desired capacity at two instances even though your application needs a minimum of a single instance to run

Maximum capacity

- You might configure the Auto Scaling group to scale out in response to increased demand, but only to a maximum of four instances

---

## Directing Traffic with Elastic Load Balancing

### Elastic Load Balancing

- AWS service that automatically distributes incoming application traffic across multiple resources such as EC2 instances
- Although ELB and Auto Scaling are seperate services, they work together to help ensure that applications runnign in EC2 can provide high performance and availability

---

## Messaging and Queuing

### Monolithic application

![](https://explore.skillbuilder.aws/files/a/w/aws_prod1_docebosaas_com/1746086400/EodoxqQXUJd_rFQ8cIsZKQ/tincan/fe470bc5add63f94f005d3da17a6db8131e78b9e/assets/CPE%20Digital%20-%20Monolithic%20application.png)

- Suppose that you have an application with tightly coupled componetns, this type of architecture can be considered a Monolithic application
- If a single componet fails, other components fail, and possibly the entire application fails

### Microservices

![](https://explore.skillbuilder.aws/files/a/w/aws_prod1_docebosaas_com/1746086400/EodoxqQXUJd_rFQ8cIsZKQ/tincan/fe470bc5add63f94f005d3da17a6db8131e78b9e/assets/CPE%20Digital%20-%20Microservices.png)

- In a microservices approach, application components are loosely coupled. If a single component fails, the other components to work because they are communicating with each other

### Amazon Simple Notification Service (Amazon SNS)

- Publish/ subscrive service
- Using SNS topics, a publisher published messages to subscribeers
- In SNS, subscribers can be web servers, email addresses, AWS Lambda functions, or several other options

### Amazon Simple Queue Service (Amazon SQS)

- Message queuing service
- You can send, and receive messages between software components, without losing messages or requiring other services to be available
- For decoupled applications and microservices, SQS enables you to send, store, and retrieve messages between components

---

## Additional Compute Services

### Serverless computing

In case of EC2

1. Provision instances
2. Upload your code
3. Continue to manage the instances while your application is running

![](https://explore.skillbuilder.aws/files/a/w/aws_prod1_docebosaas_com/1746086400/EodoxqQXUJd_rFQ8cIsZKQ/tincan/fe470bc5add63f94f005d3da17a6db8131e78b9e/assets/CPE%20Digital%20-%20Serverless%20computing.png)

- “serverless” means that your code runs on servers, but you do not need to provision or manage these servers
- Another benefit of serverless computing is the flexibility to scale serverless applications automatically

### AWS Lambda

- Service that lets you run code without needing to provision or manage servers
- You pay only for the compute time that you consume

### How AWS Lambda works

1. You upload your code to Lambda
2. You set your code to trigger form an event source, such as AWS services, mobile applications, or HTTP endpoints
3. Lambda runs your code only when triggered
4. You pan only for the compute time that you use

### Containers

- It provide you with a standard way to package your application’s code and dependencies into a single object. and you can also use containers for processes and workflows in which there are essential requirements for security, reliability, and scalability
- Container orchestration services help you to deploy, manage, and scale your containerized applications

### Amazon Elastic Container Service (Amazon EC2)

- Highly scalable, high-performance container management system that enables you to run and scale containerized applications on AWS
- Docker is a software platform that enables you to build, test, and deploy applications quickly

### Amazon Elastic Kubernetes Service (Amazon EKS)

- Fully managed service that you can use to run kubernetes on AWS
- Kubernetes is open-source software that enables you to deploy and manage containerized applications at scale

### AWS Fargate

- Serverless compute engine for containers. It works with both ECS and EKS
- You don’t need to provision or manage servers when using AWS Fragate
- You pay only for the resources that are required to run your containers