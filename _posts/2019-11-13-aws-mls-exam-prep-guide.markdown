---
layout: post
title:  "Preparing for the AWS Certified Machine Learning - Specialty Exam"
subtitle: "An exam preparation guide"
date:   2019-11-13 18:05:08 +0500
background: '/img/posts/mls-badge-logo.png'
---


This post is intended as a guide on how to prepare for the AWS Machine Learning Specialty Exam. AWS specialty exams expect at least Associate level familiarity with the AWS ecosystem. This exam is a little easy on the infrastructure as much of it is about Machine Learning in general.


The [official preparation guide](https://d1.awsstatic.com/training-and-certification/docs-ml/AWS%20Certified%20Machine%20Learning%20-%20Specialty_Exam%20Guide%20(1).pdf) by AWS is a good place to start. As per this guide, there are four key areas that the exam will test you on:

1. Data Engineering - 20%
2. Exploratory Data Analysis - 24%
3. Modeling - 36%
4. Machine Learning Implementation and Operations - 20%


## 1. Data Engineering
This domain will test how well you can use the AWS infrastructure to do 3 tasks for building ML solutions:
- **Ingest** data:
    IoT services, Amazon Kinesis, Snowball, Direct Connect are all relevant services for data ingestion. You need to understand the appropriate applications for each of these. 
- **Transform** data:
    To transform the data, depending on the application, you should understand the correct applications and possibilities for Lambda, Kinesis Data Analytics, EMR, AWS Data Pipelines, Batch Transform jobs on SageMaker, Athena, Glue
- **Store/create repositories** of data:
    You should know what data storage options are available on the AWS ecosystem for structured as well as unstructured data. Namely you should be familiar with a few services including Redshift, DynamoDB, Elasticsearch, Aurora, etc.


## 2. Exploratory Data Analysis
EDA is a really fundamental part of the Machine Learning process, and as far as this exam goes, a relatively simpler one. Here are the things that you should be comfortable with:

- **Selection of appropriate visualization techniques:**
    
    If you have some experience with Data Science or come from a maths background, this should be really simple for you.
    What kind of graphs is right for comparing time-series trends? Which visuallization would be right for comparing aggregate values accross two groups? Would a pie-chart be the apt choice if I want to see how the profits of a company have changed over the years? The list goes on..

- **Recommending tools and libraries for visualization:** 
    
    Be it the popular Python libraries (matplotlib, plotly, seaborn), or visualization libraries in other languages and frameworks (D3.js, Chart.js, React-vis, etc), you should be able to identify the appropriate solution as per the need of the problem. For instance, if someone wants to build visualizations on their webpage, D3 would be a much more logical option than plotly.

- **Dashboarding options available in AWS:**
    
    In AWS, the model training and performance metrics are sent via CloudWatch, and you can use that to visualize most of the performance aspects of a model you're training.
    If it's data that you're analysing, however, you'll need to go with either Kibana (if your data is stored in Elasticsearch), or Quicksight (if the visualization requirements are ad-hoc analysis). Do read up on what kind of access options are available with Quicksight, because it might not be the best option in every possible case, and sometimes, you might have to construe a more tailored option.

## 3. Modeling
This area on the exam is related to how well you can select a particular machine learning modeling approach for a given problem. A mix of popular machine learning algorithms, coupled with Amazon SageMaker's own built-in algorithms would be sufficient for acing this section. I am assuming you'll be familiar with:

- **Deep Learning** (Artificial Neural Networks, CNNs, RNNs)
- **Unsupervised** Techniques (PCA, KMeans, KNNs, Latent Dirichlet Analysis)
- **Supervised** Techniques (Linear/Logistic Regressions, SVMs, Decision Trees, Boosting, Bagging, etc)
- SageMaker's [**built-in algorithms**](https://docs.aws.amazon.com/sagemaker/latest/dg/algos.html) 
    - BlazingText
    - DeepAR Forecasting
    - Factorization Machines
    - Image Classification Algorithm
    - IP Insights
    - Linear Learner Algorithm
    - Neural Topic Model (NTM) Algorithm
    - Object2Vec
    - Random Cut Forest (RCF) Algorithm
    - Semantic Segmentation
    - Sequence to Sequence
- **AI Services**
    - Amazon Transcribe: Speech to text service
    - Amazon Polly: Text to speech
    - Amazon Lex: Chatbot service
    - Amazon Comprehend: NLP Understanding model
    - Amazon Forecast:
    - Amazon Translate
    - Amazon Textract
    - Amazon Personalize
    - Amazon Rekognition

## 4. Machine Learning Implementation and Operations
Along with your knowledge of Machine Learning in general, the exam will also test your understanding of what it takes to implement and deploy a ML solution on AWS.

#### SageMaker Operations
This is an important part of your capability as an AWS ML Specialist. I'll try to list the most cardinal aspects of what you should be capable to answer:
- How can you use multiple AI services to offer a solution?
- Using SageMaker to preprocess data
- How to train/prototype models in SageMaker using built-in algorithms ([Build models](https://docs.aws.amazon.com/sagemaker/latest/dg/build-model.html))
- Using custom code to build models ([Elastic Container Registry](https://aws.amazon.com/ecr/))

#### Supported ML Frameworks
SageMaker supports a variety of ML frameworks:
![Supported Frameworks](/img/posts/aws_supported_frameworks.png)
AWS doesn't expect you to be master of all these supported frameworks; what's expected, however, is that you're at least familiar with these, and know what each is capable of. The Linux Academy course (see Available Learning Resources) offers a few introductory toy problems in Tensorflow, Pytorch and MXNet.

#### Compute Infrastructure
It's pertinant to understand how to select the correct instance types for different kinds of applications. A transformation job running on EMR will have different instance type demands than a Deep Learning distributed job running with a parameter server. See [instance types](https://aws.amazon.com/sagemaker/pricing/instance-types/) for more information and understand which type is relevant for different use-cases.




## Available learning resources:

### Linux Academy:
The Linux Academy course is right for you if you want to be shown the basics of the AWS ecosystem. The course will give you an overview of all the AWS specific services, and the most basic limitations and antipatterns for each service. The only thing I dislike about this is it goes into discussing Machine Learning concepts, wheareas if you're already a ML practitioner, you'd be skipping this part.


### AWS Documentation: 
The [documentation](http://aws.amazon.com/documentation) will be your best friend for more complicated stuff, and is highly recommended for anything you find complicated even after going through the videos.


### AWS Official Free Courses:
On the AWS training website, you can find a bunch of free digital learning material. This material is officially produced with the test in mind, and hence is usually high quality. However, for this specialty there isn't much of exam readiness material.

#### ML Building Blocks: Services and Terminology: 
This course will explain some general ML terminologies and concepts that you should know. If you are already comfortable with Machine Learning, you can skip this one, because it is about the Machine Learning process and what happens each step of the way.
The course is available [here](https://www.aws.training/Details/Curriculum?id=27242).

### Whitepapers
While there is a wide range of whitepapers available on the AWS website, I would not recommend investing time in reading these. The time investment is not worth the exam-relevant knowledge gained. The papers are written at a superficial level of abstraction that would not help much with the problems that come up on the exam.

## Test yourself before the exam
You should get plenty of practice before you take the exam. I would normally suggest going for some practice tests that a vendor like Linux Academy provides. However, if you are a seasoned ML professional, the free resources below should be sufficient to get a handle on how much difficult the exam will be (not much).

The AWS official website for the ML Specialty contains [sample questions](https://d1.awsstatic.com/training-and-certification/docs-ml/AWS-Certified-Machine-Learning-Specialty_Sample-Questions.pdf).

Whizlabs also provides a [free test](https://www.whizlabs.com/aws-certified-machine-learning-specialty/). You can purchase their exam bundle if you'd like.

Good luck with your exam!

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
