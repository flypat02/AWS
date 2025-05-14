# day8)Migration

## AWS Cloud Adoption Framework (AWS CAF)

- CAF organized guidance into six areas of focus, called Perspectives
- Business, People, Governance Perspectives focus on business capabilities
- Platform, Security, Operations Perspectives focus on technical capabilities

### Business Perspective

- Ensures that IT aligns with business needs and that IT investments link to key business results
- Common roles in the Business Perspective include:
1. Business managers
2. finance managers
3. Budget owners
4. Strategy stakeholders

### People Perspective

- Supports development of an organization-wide change management strategy for successful cloud adoption
- Common roles in the people perspective include:
1. Human resources
2. Staffing
3. People managers

### Governance Perspective

- Focuses on the skills and processes to align IT strategy with business strategy
- Common roles in the Governance Perspective include:
1. Chief Information Officer (CIO)
2. Program managers
3. Enterprise architects
4. Business analysts
5. Portfolio managers

### Platform Perspective

- Includes principles and patterns for implementing new solutions on the cloud, and migrating on-premises workloads to the cloud
- Common roles in the Platform Perspective include:
1. Chief Technology Officer (CTO)
2. IT managers
3. Solutions architects

### Security Perspective

- Ensures that the organization meets security objectives for visibility, auditability, control, and agility
- Common roles in the Security Perspective include:
1. Chief Information Security Officer (CISO)
2. IT security managers
3. IT security analysts

### Operations Perspective

- Helps you to enable run, use, operate, recover IT workloads to the level agreed upon with your business stakeholders
- Common roles in the Operations Perspective include:
1. IT operations managers
2. IT support managers

---

## 6 Strategies for migration

- When migrating applications to the cloud, six of the most common migration strategies that you can implement
1. Rehosting
2. Replatforming
3. Refactoring/re-architecting
4. Repurchasing
5. Retaining
6. Retiring

### Rehosing

- “lift-and-shift” involves moving applications without changes

### Replatforming

- “lift,tinker, and shift” involves making a few cloud optimizations to realize a tangible benefit

### Refactoring/re-architecting

- Involves reimagining how an application is architected and developed by using cloud-native features

### Repurchasing

- Involves moving from a traditional license to a software-as-a-service model

### Retaining

- Consists of keeping applications that are critical for the business in the source environment
- This might include applications that require major refactoring before they can be migrated, or work that can be postpones until a later time

### Retiring

- The process of removing applications that are no longer needed

---

## AWS Snow Family members

- A collection of physical devices that help to physically transport up to exabytes of data into and out of AWS
- AWS Snowcone, AWS Snowball, AWS Snowmobile

![](https://explore.skillbuilder.aws/files/a/w/aws_prod1_docebosaas_com/1747242000/wL1vwo0M9Z7SLrpZad7hxA/tincan/fe470bc5add63f94f005d3da17a6db8131e78b9e/assets/snow%20family.jpg)

### AWS Snowcone

- Small, regged, secure edge computing and data transfer device
- It features 2 CPUS, 4GB of memory, up to 14TB of usable storage

### AWS Snowball

- Two categories of snowball
1. Snowball Edge Storage Optimized
-Devices are well suited for large-scale data migrations and recurring tranfer workflows
-Storage: 80TB HDD, 1TB SSD
-Compute: 40vCPUs, 80GB of memory to support EC2 1 instances
2. Snowball Edge Compute Optimized
-Provides powerful computing resources for use cases such as machine learning, full motioon video
-Storage: 80TB HDD S3, EBS and 28TB SSD,EBS
-Compute: 104vCPUS, 416GB of memory, optional NVIDIA Tesla V100 GPU