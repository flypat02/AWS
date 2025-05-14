# Practitioner Essentials 2일차

## Selecting a Region

- When determining the right Region for you services, consider the following four business factors

### Compliance with data governance and legal requirements

- Depending on your company and location, you might need to run your data out of specific area.
- Companies have location-specific data regulations

### Proximity to your customers

- Selecting a Region that is close to your customers will help you to get content to them faster

### Available services within a Region

- Sometimes, the closest Region might not have all the features that you want to offer to customers.
- You would have to run it in one of the Regions that already offers it

### Pricing

- You will learn in more detail that several factors determin pricing, but for now know that the cost of services can vary from Region to Region

---

## Availability Zones

![](https://explore.skillbuilder.aws/files/a/w/aws_prod1_docebosaas_com/1746198000/doVho57Z8B-KL5gAccEb5w/tincan/fe470bc5add63f94f005d3da17a6db8131e78b9e/assets/availability_zones.png)

- Availability Zones is a single data center or a group of data centers within a Region
- AZ are located tens of miles apart from each other
- This is close enough to have low latency between AZ

### EC2 instances in multiple AZ

- Planning for failure and deploying applications across multiple AZ is an important part of building a resilient and highly available architecture

---

## Edge locations

- A site that Amazon CloudFront uses to store cached copies of your content closer to your customers for faster delivery

### Edge locations Scenario

1. Suppose that your company’s data is stored in Brazil, and you have customers who live in China. you don’t need to move all the content to one of the Chinese Regions
2. You can cache a copy locally at an edge location that is close to your customers in China
3. When a customer in China requests one of our files, Amazon CloudFront retreves the file form the cache in the edge location and delivers the file to the customer

---

## Ways to interact with AWS services

- API: Application Programming Interface, there are pre determined ways for you to interact with AWS

### AWS Management Console

- A web-based interface for accessing and managing AWS services

### AWS Command Line Interface

- Enalbes you to control multiple AWS services directly from the command line within one tool

### Software Development Kits

- SDKs make it easier for you to use AWS services through an API designed for your programming langugage or platform

### AWS Elastic Beanstalk

- You provide code and configuration settings, and Elastic Beanstalk deploys the resources necessary to perform the following tasks:
1. Adjust capacity
2. Load balancing
3. Automatic Scaling
4. Application health monitoring

### AWS CloudFormation

- You can treat your infrastructure as code.
- You can build an environment by writing lines of code instead of using the AWS Management Console to individually provison resources
- Provisions your resources in a safe, repeatable manner, enabling you to frequently build your infrastructure and applications without having to perform manual acations