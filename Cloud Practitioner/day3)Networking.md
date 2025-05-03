# Practitioner Essentials 3일차

## Amazon Virtual Private Cloud (Amazon VPC)

- Enables you to provision an isolated section of the AWS cloud
- In this isolated section, you can launch resources in a virtual network that you define

### Subnet

- Subnet is a section of a VPC that cna contain resources such as Amazon VPC instances

## Internet gateway

![](https://explore.skillbuilder.aws/files/a/w/aws_prod1_docebosaas_com/1746280800/3OMkf4QRmRF9VP8-PVX09Q/tincan/fe470bc5add63f94f005d3da17a6db8131e78b9e/assets/CPE%20Digital%20-%20Module%204%20-%20Internet%20Gateway.png)

- An arrow connects the client to the gateway over the internet indicating that the clinet’s request has gained access to the VPC
- Connection between a VPC and the internet

## Virtual private gateway

- The component that allows protected internet traffic to enter into the VPC
- Enable you to establish a VPN connection between your VPC and a private network, such as an on-premises data center or internal corporate network
- A virtual gateway allows traffic into the VPC only if it is coming from an approved network

## AWS Direct Connect

- A service that lets you to establish a dedicated private connection between your data center and VPC

![](https://explore.skillbuilder.aws/files/a/w/aws_prod1_docebosaas_com/1746280800/3OMkf4QRmRF9VP8-PVX09Q/tincan/fe470bc5add63f94f005d3da17a6db8131e78b9e/assets/CPE%20Digital%20-%20Module%204%20-%20AWS%20Direct%20Connect.png)

- A corporated data center routes network traffic to an AWS Direct Connect location. That traffic is then routed to a VPC through a virtual privated gateway. All network traffic between the corporate data center and VPC flows through this dedicated privated connection

---

# Subnets and Network Access Control Lists

## Subnets

- A section of a VPC in which you can group resources based on security or operational need
- subnets can be public or private
- In a VPC, subnets cna communicate with each ohter

### Public subnets

- Contain resources that need to be accessible by the public

### Private subnets

- Contain resources that should be accessible only through your private network

## Network traffic in a VPC

### Packet

- A unit of data sent over the internet or a network
- The VPC component that checks packet permissions for subnets is a network access control list

## Network ACLs

- A virtual firewall that control inbound and outbound traffic at the subnet level
- By default, your account’s default network ACL allows all inbound and outbound traffic
- You can modify it by adding your own rules, all network ACLs have an explicit deny rule

## Stateless packet filtering

- NACLs perform stateless packet filtering
- They remember nothing and check packets that cross the subnet border each way: inbound and outbound

![](https://explore.skillbuilder.aws/files/a/w/aws_prod1_docebosaas_com/1746280800/3OMkf4QRmRF9VP8-PVX09Q/tincan/fe470bc5add63f94f005d3da17a6db8131e78b9e/assets/CPE%20Digital%20-%20Module%204%20-%20Network%20ACL%202.png)

## Security groups

- Virtual firewall that controls inbound and outbound traffic for an EC2 instance
- By default, a security group denies all inbound traffic and allows all outbound traffic
- You can custom rules to configure which traffic should be allowed

## Statedful packet filtering

- Security groups perform stateful packet filtering
- They remember previous decisions made for incoming packets

![](https://explore.skillbuilder.aws/files/a/w/aws_prod1_docebosaas_com/1746280800/3OMkf4QRmRF9VP8-PVX09Q/tincan/fe470bc5add63f94f005d3da17a6db8131e78b9e/assets/CPE%20Digital%20-%20Module%204%20-%20Security%20group%202.png)

### Blueprint of VPC

![](https://explore.skillbuilder.aws/files/a/w/aws_prod1_docebosaas_com/1746280800/3OMkf4QRmRF9VP8-PVX09Q/tincan/fe470bc5add63f94f005d3da17a6db8131e78b9e/assets/CPE%20Digital%20-%20Module%204%20-%20Network%20traffic%20in%20a%20VPC.png)

---

## Domain Name System (DNS)

- The process of translating a domain name to an IP address

### How to visit AnyCompany’s website

1. When you enter the domain name into your browser, this request is sent to a customer DNS resolver
2. The customer DNS resolver asks the company DNS server for the IP address that corresponds to AnyCompany’s website
3. The company DNS server responds by providing the IP address for AnyCompany’s website 

## Amazon Route 53

- A DNS web service, It gives developers and businesses a reliable way to route end users to internet applications hosted in AWS
- Connects user requests to infrastructure running in AWS and it can route users to infrastructure outsid of AWS
- THE ability to manage the DNS records for domain names