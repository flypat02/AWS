# Practitioner Essentials 4일차

# Instance Stores and Amazon Elastic Block Store (Amazon EBS)

## Instance stores

- Provides temporary block-level storage for EC2 instance
- Instance store is disk storage that is physically attached to the host computer for an EC2 instance
- When the instance is terminated, you lose any data in the instance store

## Amazon Elastic Block Store (EBS)

- Service that provides block-level storage volumes that you can use with EC2 instance
- If you stop or terminate an EC2, all the data on the attached EBS volume remains available
- You defiine the configuration and provision it

## Amazon EBS snapshots

![](https://explore.skillbuilder.aws/files/a/w/aws_prod1_docebosaas_com/1746720000/eLqKV9n7VXWP38MQV0E6Jg/tincan/fe470bc5add63f94f005d3da17a6db8131e78b9e/assets/EBS_snapshots.png)

- Incremental backup. This means that the first backup taken of a volume copies all the data

---

## Object storage

![](https://explore.skillbuilder.aws/files/a/w/aws_prod1_docebosaas_com/1746720000/eLqKV9n7VXWP38MQV0E6Jg/tincan/fe470bc5add63f94f005d3da17a6db8131e78b9e/assets/object_storage.png)

- Each object consists of data, metadata, and a key
- Metadata contains information about what the data is how it is used, the object size, and so on
- An object’s key is its unique identifier

#Recall tha twhen you modify a file in block storage, only the pieces that are changed are updated.
   When a file in object storage is modified, the entire object is updated

## Amazon Simple Storage Service (Amazon S3)

- Service that provides object-level storage
- S3 stores data as objects in buckets
- The mazimum file size for an object in S3 in 5TB
- You cna use the S3 versioning feature of track changes to your objects over time

## Amazon S3 storage classes

- You choose from a range of storage classes to select a fit for your business and cost needs
- When selecting an S3 storage class consider that How often you plan to retrieve your data, How available you need your data to be
- Different eight categories
    - S3 Standard
    -Designed for frequently accessed data
    -Stores data in a minimum of three AZs
    - S3 Standard-Infrequent Access (S3 Standard-IA)
    -Ideal for infrequently accessed data
    -Similar to S3 Standard but has a lower storage price and higher retrieval price
    - S3 One Zone-Infrequent Access (S3 One Zone-IA)
    -Stores data in a single AZ
    -Has a lower storage price than S3 Standard-IA
    - S3 Intelligent-Tiering
    -Ideal for data with unknown or changing access patterns
    -Requires a small monthly monitoring and automation fee per object
    - S3 Glacier Instant Retrieval
    -Works well for archived data that requires immediate access
    -Can retrieve objects within a few milliseconds
    - S3 Glacier Flexible Retrieval
    -Low-cost storage designed for data archiving
    -Able to retrieve objects within a few minutes to hours
    - S3 Glacier Deep Archive
    -Lowest-cost object storage class ideal for archiving
    -Able to retrieve objects within 12 hours
    - S3 Outposts
    -Creates S3 buckets on S3 Outposts
    -Makes it easier to retrieve, store, and access data on AWS Outposts

---

## File Storage

- Multiple clients can access data that is stored in shared file folders
- Compard to block storage and object storage, file storage is ideal for use cases in which a large number of services and resources need to access the same data at the same time

## Amazon Elastic File System (Amazon EFS)

- A scalable file system used with AWS Cloud services and on-premises resources
- You can add and remove files, EFS grows and shrinks automatically

## Comparing EBS and EFS

- EBS
    - An EBS volume stores data in a single AZ
    - To attach an EC2 instance to an EBS volume, both the EC2 instance and EBS volume must reside within the same AZ
- EFS
    - EFS is a regional service. It stores data in and across multiple AZ
    - The duplicate storage enables you to access data concurrently from all the AZ in the Region where a file system is located
    - Additionally, on-premises servers can access EFS using AWS Direct Connect

---

## Relational databases

- In a relational database, data is stored in a way that relates it to other pieces of data
- Relational databases use SQL to store and query data

## Amazon Relational Database Service (RDS)

- A service that enables you to run relational databases in the AWS Cloud
- Managed service that automates tasks such as hardware provisioning, database setup, patching, and backups
- Many Amazon RDS database engines offer encryption at rest and encryption in transit

## Amazon RDS database engines

- Available on six database engines
1. Amazon Aurora
2. PostgreSQL
3. MySQL
4. MariaDB
5. Oracle Database
6. Microsoft SQL Server

## Amazon Aurora

- An enterprise-class relational database. It is compatible with MySQL and PostgreSQL relational databases
- Aurora helps to reduce your database costs by reducing unnecessary I/O operations
- It replicates six copies of your data across three AZs and continuously backs up your data to S3

---

## Nonrelational databases

- You can create tables. A table is a place where you can store and query data
- NoSQL databases use key-value pairs. With key-value pairs, data is organized into items (keys), and items have attributes (values)
- In a key-value database, you can add or remove attributes from items in the table at any time

## Amazon Dynamo DB

- Key-value database service. It delivers single-digit millisecond performance at any scale
- Features of DynamoDB
    - Serverless
    -DynamoDB is a serverless, which means that you do not have to provision, patch, manage servers, install, maintain, and operate software
    - Automatic Scaling
    -DynamoDB automatically scales to adjust for changes in capacity while maintaining consistent performance

---

## Amazon Redshift

- A data warehousing service that you can use for big data analytics
- It offers the ability to collect data from many sources and helps you to understand relationships and trends across your data
- It fit in Bigdata BI

---

## Aws Database Migration Service (AWS DMS)

- Enables you to migrate relational databases, nonrelational databases, and other types of data stores
- You move data between a source DB, and target DB. The source and target DB can be of the same type or different types

## Other use cases for AWS DMS

### Development and test database migrations

- Enabling developers to test applications against production data without affecting production users

### Database consolidation

- Combining several databases into a single database

### Continuous replication

- Sending ongoing copies of your data to other target sources instead of doing a one-time migration

---

## Additional database services

### Amazon DocumentDB

- A document database service that supports MongoDB workloads.

### Amazon Neptune

- A graph database service
- You can use Neptune to build and run applications that work with highly connected datasets, such as recommendation engines, fraud detection, and knowledge graphs

### Amazon Qunatum Ledger Database (Amazon QLDB)

- A ledger database service
- You can use QLDB to review a complete history of all the changes that have been made to your application data

### Amazon Managed Blockchain

- A service that you can use to create and manage blockchain networks with open-source frameworks
- Blockchain is a distributed ledger system that lets multiple parties run transactions and share data without a central authority

### Amazon ElasticCache

- A service that adds caching layers on top of your databases to help improve the read times of common requests
- It supports two types of data sotres: Redis and Memcached

### Amazon DynamoDB Accelerator

- An in-memory cache for DynamoDB
- It helps improve response times from single-digit milliseconds to microseconds