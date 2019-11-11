---
layout: post
title:  "Preparing for the AWS Certified Big Data - Specialty Exam"
subtitle: "An exam preparation guide"
date:   2019-11-01 18:05:08 +0500
background: '/img/posts/bds-badge-logo.png'
---


This post is intended as a guide on how to prepare for the AWS Big Data Specialty Exam. AWS specialty exams expect at least Associate level familiarity with the AWS ecosystem. 

## Big Data Specialty: Key Areas
If you read up the <a href="https://d1.awsstatic.com/training-and-certification/docs-bigdata-spec/AWS%20Certified%20Big%20Data%20-%20Specialty_Exam%20Guide_v1.4_FINAL.pdf">AWS Big Data - Specialty Exam Guide</a> provided by AWS, you'll find that there are six domains the exam comprises, and the composition of the exam:

1. Collection - 17%
2. Storage - 17%
3. Processing - 17%
4. Analysis - 17%
5. Visualization - 12%
6. Data Security - 20%

I will discuss these core domains one by one, talking about the relevant services and question types that will be most useful to understand.

## The essential hidden domain
Despite there being 6 domains, there is an essential domain in the AWS Big Data - Specialty exam that is most essential: the Hadoop family. The following list is not exhaustive, but these technologies will turn up on the exam some way. 

- Hadoop
- Spark
- Kafka
- Hive
- Pig
- HBase
- Impala
- Mahout
- Oozie
- Zoo Keeper
- Flume
- Cassandra
- Sqooq
- Ambari

While a deep knowledge of these technologies is not required, an understanding of the functionality of these tools and their correct applications is something that will help you a lot.

### Collection:
The following AWS services are exam-relevant from the collection domain:

- **IoT**
    - You should know what **Greengrass** is.
    - You should know about IoT **Rules** and **Actions**
    - Know the different ways to **authenticate** for IoT

- **Kinesis**
    - Know where Kinesis is better, and where Spark Streaming on EMR or some other alternative is better
    - **Data retention limitations** - Know what's the maximum **time** that Kinesis can retain data
    - What's the maximum **size** of data that Kinesis can hold
    - When does it make sense to change the number of shards? (**Producer, Consumer and Networking limitations** per shard)

- **Direct Connect**
    - When does it make sense to use direct connect to migrate data to AWS
    - What **security** steps can you take to secure this connection

- **Snowball**
    - **Latency** of data transfer
    - When is snowball a good choice

- **Database Migration Service**
    - Types of **DB systems** that can be migrated
    - Compatible migration **targets**

- **SQS and SNS**
    Just a cursory glance at the documentation should set you up for these. Though most questions will have better alternatives for these choices, there will be the rare case, you'll need to use these.

### Storage:
- **S3**
    - Know the **data lifecycle** rules you can set
    - **Glacier** storage
    - Data accidental **deletion** protection (common trick question type)
    - File **versioning** in S3 is also a relevant topic that might show up in a question

- **DynamoDB**
    - Keep in mind that DynamoDB is **not for analytics** (trick questions can occur)
    - Read and Write **capacity** units and **limitations**
    - **Read consistency** limitations
    - Data **partitioning** (you might have to select which keys to partition on for a use case)
    - Using **DAX** (DynamoDB Accelerator) correctly

### Processing
- **EC2**
    This is the basis of processing in AWS.
- **Amazon EMR**
    - [**Differences** between Apache Hive on EMR and Apache Hive](https://docs.aws.amazon.com/emr/latest/ReleaseGuide/emr-hive-differences.html)
    - **EMR File System**
    - **Authorization** limitations

- **Amazon Machine Learning** and **Sagemaker**
    For Machine Learning related applications, you will need to know about these two most popular services AWS provides in that domain.
    - Remember which Machine Learning tasks are possible in AML
    - There will be questions about missing data labels in datasets for use with AML
    - For most other complex modeling needs, Sagemaker will be the choice, and you will not need to know the details of the algorithms available or even how Sagemaker operates for that matter
- **Lambda**
    - Timeout and memory limitations are important, as well as the services that you can connect to Lambda
    - Read up a bit on AWS Step Functions
- **AWS Data Pipeline**
    This will be a frequent choice to turn up for ETL related questions, so you should understand: 
    - how it operates
    - the languages supported
    - the infrastructure it uses
    - the compatible data sources and sinks
    - time limitations
- **AWS Glue**
    This is also a frequent choice to appear in ETL related questions. The most important things to consider in this service are:
    - Glue Data Catalog and how it can integrate with other services in the AWS ecosystem
    - Using with EMR Apache Hive: can serve as a metastore

### Analysis
The following services form the Analysis domain of the exam:
- **Athena**
- **Redshift**
- **Elasticsearch**
- **Kinesis Analytics**

These services have a lot of nitty-gritty details that you will need to go over, and the topics are just too many to list down in this guide. Even if you follow video lectures, I would still recommend skimming over all the documentation to get a gist of which technicalities exist, and reading in detail the topics you are least comfortable with.

Generally, you should know:
- which services are better for ad-hoc analysis
- when is scale and data volume a constraint in service selection
- if you need availability or replication across different zones, how do you achieve that in any of these services

### Visualization
- Understand how **Quicksight** works
- Know what **Kibana** is capable of and where does it make sense to use it
- In which cases can we have visualizations and **reporting** against our AWS services directly from the console
- Know **common data visualization libraries** for front-end: D3.js, Highcharts, etc
- Where does it make sense to generate static graphs stored as image files
- Correct **visualization types** for different usecases: line charts, pie charts, bar charts, etc

### Data Security
Since security is an important theme in the Big Data - Specialty exam, you will see lots of service specific topics in each domain, and while that covers a sizable chunk of the questions that will come up in this domain, I would recommend reading the AWS documentation relevant to the following:
- IAM
- Identity Federation
- S3 **ACLs**
- Data **Encryption** at-rest & in-transit
- AWS **KMS**
- **Local KMS integration** possibilities with AWS services
- **Authentication** Protocols (e.g. Kerberos)
- User level **access control in DB** services, Redshift, and Quicksight

## Available learning resources:

### Linux Academy:
The [Linux Academy course](https://linuxacademy.com/course/aws-certified-big-data-specialty-course) is right for you if you want to be shown the basics of the AWS ecosystem. The course will give you an overview of all the AWS specific services, and the most basic limitations and antipatterns for each service.


### AWS Documentation: 
The [documentation](http://aws.amazon.com/documentation) will be your best friend for more complicated stuff, and is highly recommended for anything you find complicated even after going through the videos.


### AWS Official Free Courses:
On the AWS training website, you can find a bunch of free digital learning material. This material is officially produced with the test in mind, and hence is high quality. Highly recommended to go through this before attempting the exam.

#### Data Analytics Fundamentals: 
This course teaches you about the right kind of 
The course is available [here](https://www.aws.training/learningobject/wbc?id=35364).

#### Exam Readiness: AWS Big Data - Specialty (Digital): 
This one is a must before attempting the exam. It has a few Big Data use cases in different application domains (e.g. Finance, Health etc.) which are
highly relevant to the types of use cases that will turn up on the exam. A few common question types are also discussed, which will give you a true idea of the difficulty level of the actual exam.
The course is available [here](https://www.aws.training/Details/Curriculum?id=21332).

### Whitepapers
While there is a wide range of whitepapers available on the AWS website, I would not recommend investing time in reading these. The time investment is not worth the exam-relevant knowledge gained. The papers are written at a superficial level of abstraction that would not help much with the problems that come up on the exam.


[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
