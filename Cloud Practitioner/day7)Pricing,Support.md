# Practitioner Essentials 7일차

## AWS Free Tier

- Enables you to begin using certain services without having to worry about incurring costs for the specified period
1. Always Free
-These offers do not expire and are available to all AWS customers
2. 12 months Free
-These offers are free for 12 months following your initial sign-up date to AWS
3. Trials
-Short-term free offers start from the date you activate a particular service

---

## AWS Pricing Concepts

- AWS offers a range of cloud computing services with pay-as-you-go pricing

### Pay for what you use

- You pay for exactly amount of resources that you actually use, without requiring long-term contracts or complex licensing

### Pay less when you reserve

- Some services offer reservation options that provide a significant discount compared to On-Demand instance pricing

### Pay less with volume-based discounts when you use more

- Some services offer tiered pricing, so the per-unit cost is incrementally lower with increased usage

## AWS Pricing Calculator

- Lets you explore AWS services and create an estimate for the cost of your use cases on AWS

## AWS pricing examples

### AWS Lambda

- You are charged based on the number of requests for your functions and the time that it takes for them to run
- Allows 1 million free requests and up to 3.2 million seconds of compute time per month
- Saving plan 1-year or 3-year term

### Amazon EC2

- You pay for only the compute time that you use while your instances are running
- You can find additional cost savings for EC2 by considering Savings Plans and Reserved Instances

### Amazon S3

- Storage: you pay for only the storage that you use
- Requests and data retrievals: you pay for requests made to your S3 objects and buckets
- Data transfer: There is no cost to transfer data between different S3 or from S3  to other services within the same AWS region, data transferred into S3 from the internet or out to CloudFront, data transferred out to an EC2 instance in the same AWS Region as S3 bucket. Pay for data the you transfer into and out of S3 with a few exceptions
- Management and replication: You pay for the storage management features that you have enabled on your account’s S3 buckets

---

## Consolidated billing

- AWS Organizations also provides the option for consolidated billing
- The consolidated billing feature of Organizations enables you to receive a single bill for all AWS accounts in your organization
- The default maximum number of accounts allowed for an organizations is 4, but you can increase your quota

---

## AWS Budgets

- You can create budgets to plan your service usage, service costs, and instance reservations
- You can also set custom alerts when your usage szceeds the budgeted amount

---

## AWS Cost Explorer

- A tool tha tlets you visualize, understand, and manage your AWS costs and usage over time

---

## AWS Support

- AWS offers four different Support plans to help you troubleshoot issues, lower costs and efficiently use AWS services
1. Basic
2. Developer
3. Businees
4. Enterprise On-Ramp
5. Enterprise

### Basic support

- Free for all customers. It includes access to whitepapers, documentation, and support communities
- You have access to a limited selection of AWS Trusted Advisor checks
- You can use the AWS Personal Health Dashboard

### Developer Support

- Best practice guidance
- Client-side diagnostic tools
- Building-block architecture support, which consists of guidance for how to use AWS offerings, features, and services together

### Business Support

- Use-case guidance to identify AWS offerings, features, and services that can best support your specific needs
- All AWS Trusted Advisor checks
- Limited support for third-party software

### Enterprise On-Ramp Support

- A pool of Technical Account Managers to provide proactive guidance and coordinate access to programs and AWS experts
- A cost Optimization workshop (one per year)
- Tools to monitor costs and performance through Trusted Advisor and Health API/Dashboard
- A Concierge support team for billing and account assistance
- Consultative review and architecture guidance (one per year)
- Infrastructure Event Management support (one per year)
- Support automation workflows
- 30 minutes or less response time for business-critical issues

### Enterprise Support

- A designated Technical Account Manager to provide proactive guidance and coordinate access to programs and AWS experts
- A Concierge support team for billing and account assistance
- Operations Reviews and tools to monitor health
- Training and Game Days to drive innovation
- Tools to monitor costs and performance through Trusted Advisor and Health API/Dashboard
- Consultative review and architecture guidance
- Infrastructure Event Management support
- Cost Optimization Workshop and tools
- Support automation workflows
- 15 minutes or less response time for business-critical issues

## Technical Account Manager (TAM)

- Tams provide expert engineering guidance, help you design solutions that efficiently intergrate AWS services

---

## AWS Marketplace

- A digital catalog that includes thousands of software listings from independent software vendors
- You can use AWS Marketplace to find, test, and buy software that runs on AWS