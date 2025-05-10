# Practitioner Essentials 5일차

## The AWS shared responsibility model

- The shared responsibility model divides into customer responsibilities (security in the cloud), and AWS responsibilities (security of the cloud)

![](https://explore.skillbuilder.aws/files/a/w/aws_prod1_docebosaas_com/1746882000/l3NDz_fsU8PvVpsSNxYnow/tincan/fe470bc5add63f94f005d3da17a6db8131e78b9e/assets/Module%206_AWS%20Shared%20Responsibility%20Model%20Lesson_%20AWS%20SRM%20Image.png)

### Customers: Security in the cloud

- Customers are responsible for the security of everything that they create and put in the AWS Cloud
- When using AWS services, the customer maintain complete control over your content, how access rights are granted, managed, and revoked

### AWS: Security of the cloud

- AWS operates, manages, and controls the components at all layers of infrastructure
- This includes areas such as the host operating system, the virtualization layer, and even the physical security of the data centers from which services operate

---

## AWS Identity and Access Management (IAM)

- Enables you to manage access to AWS services and resources securely
- IAM gives you the flexibility to configure access based on your company’s specific operational and security needs

### AWS account root user

- When you fisrt crate an AWS account, you begin with an identity known as the root user
- The root user is accessed by signing in with the email address and password that you used to create your AWS account

![](https://explore.skillbuilder.aws/files/a/w/aws_prod1_docebosaas_com/1746882000/l3NDz_fsU8PvVpsSNxYnow/tincan/fe470bc5add63f94f005d3da17a6db8131e78b9e/assets/CPE%20Digital%20-%20AWS%20account%20root%20user.png)

### IAM users

- An identity that you create in AWS
- It represents the person or application that interacts with AWS services and resources
- By default, new IAM user in AWS, it has no permissions associated with it

### IAM policies

- A document that allows or denies permissions to AWS services and resources
- IAM policies enable you to customize user’s levels of resources

### IAM groups

- IAM group is a collection of IAM users
- When you assign an IAM policy to a group, all users in the group are granted permissions specified by the policy

### IAM roles

- IAM role is an identity that you can assume to gain temporary access to permissions
- When someone assumes an IAM role, they abandon all previous permissions that they had under a previous role and assume the permissions of the new role
- Example of IAM roles
    1. First the coffee shop owner grants the employee permissions to the “Cashier” and “Inventory” roles so they can switch between these two workstations
    2. The employee begins their day by assuming the “Cashier” role. This grants them access to the cash register system
    3. Later in the day, the employee needs to update the inventory system. They assume the “Inventory” role

### Multi-factor authentication (MFA)

- In IAM, MFA provides an extra layer of security for your AWS account
- 아이디와 비밀번호 이외로 전화번호로 개인 인증 하는 것이 MFA의 예

---

## AWS Oragnizations

- Consolidate and manage multiple AWS accounts within a central location
- When you create an organization, AWS Organizations automatically creates a root, which is the parent container for all the accounts in your organization
- By using Service Contorl Policies(SCPs), you can centrally control permissions for the accounts in your organization. SCPs enable you to place restrictions on the AWS services, resources, and individual API actions that users and roles in each account can access

## Organizational units

- You can group accounts into organizational units(OUs) to make it easier to manage accounts with similar business or security requirements

---

## AWS Artfact

- A service that provides on-demand access to AWS security and compliance reports and select online agreements

### AWS Artifact Agreements

- In Artifact Agreements, you can review, accept, and manage agreements for an individual account and for all your accounts in AWS Organizations

### AWS Artifact Reports

- Provide compliance reports from third-party auditors. These auditors have tested and verified that AWS is compliant with a variety of global, regeional, and industry-specific security standards and regulations

## Customer Compliance Center

- Contains resources to help you learn more about AWS compliance

---

## Denial-of-service attacks (DOS)

![](https://explore.skillbuilder.aws/files/a/w/aws_prod1_docebosaas_com/1746882000/l3NDz_fsU8PvVpsSNxYnow/tincan/fe470bc5add63f94f005d3da17a6db8131e78b9e/assets/DoS%20attack.png)

- Deliberate attempt to make a website or application unavailable to users

## Distributed denial-of-service attacks(DDOS)

![](https://explore.skillbuilder.aws/files/a/w/aws_prod1_docebosaas_com/1746882000/l3NDz_fsU8PvVpsSNxYnow/tincan/fe470bc5add63f94f005d3da17a6db8131e78b9e/assets/DDoS%20attack.png)

- DDOS attack, multiple sources are used to start an attack that aims to make a website or application unavailable

## AWS Shield

- A service that protects applications against DDOS attacks

### AWS shield Standard

- Automatically protects all AWS customers at no cost
- It protects your AWS resources from the most common, frequently occuring types of DDos attacks

### AWS Shield Advanced

- A paid service that provides detailed attack diagnostics and the ability to detect and mitigate sophisticated DDos attacks

---

## AWS Key Management Service (AWS KMS)

- Enables you to perform encryption operations through the use of cryptographic keys.
- A cryptographic key is a rnadom string of digits used for encrypting and decrypting data
- With KMS, you can choose the specific levels of access control that you need for your keys

## AWS WAF

- Web application firewall that lets you monitor network requests that come into your web applications

## Amazon Inspector

- Helps to improve the security and compliance of applications by running automated security assessment

## Amazon GuardDuty

- A service that provides intelligent threat detection for your AWS infrasturcure and resources