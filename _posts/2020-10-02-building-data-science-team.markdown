---
layout: post
title:  "Putting together a capable Data Science team"
subtitle: "The roles, market norms, and seeing value behind the ostentatious titles"
date:   2020-10-02 18:05:08 +0500
background: '/img/posts/ds-team.jpg'
---

The other day, I was interviewing candidates for a Machine Learning role, specifically someone for productionizing ML models and pipelines. The way I approach interviews is to look for the things in the candidate's CV that fits the role and drive the conversation around them. At the end of the day, reviewing my feedback for each applicant, I noticed a compelling problem with the candidates. Here is how I'd describe each one of them briefly:
- Candidate A: Research background, strong grip in theory and mathematics, but no experience whatsoever in deploying and productionizing ML models, specializes in capsule networks and computer vision problems
- Candidate B: A few years of experience in the industry, very feeble understanding of core concepts, and could not explain what he did and how, but has bragging rights to performing good in AWS and Microsoft hackathons
- Candidate C: Working in a bank with the risk analysis team, proficient with BI tools and reporting, knows just enough Machine Learning to be a plausible candidate

Now all candidates have distinctive skills which do overlap a little, but they all call themselves Data Scientists. This made me think if there should be a better nomenclature to tell them apart. In terms of skills, there is a somewhat clearer taxonomy, which, for better or for worse, the industry doesn't seem to adhere to, specially in the somewhat evolving market of Pakistan.

## The Data Hierarchy of Needs
To talk about this taxonomy, let me refer to the data hierarchy of needs. Data begins the journey from instrumentation and logging; gets collected, moved and stored; is transformed and experimented with; gets cleaned and analyzed; and eventually it is used to learn models and produce insights to help businesses.
<!-- <img src="https://hackernoon.com/hn-images/1*7IMev5xslc9FLxr9hHhpFw.png" alt="drawing" width="600"/> -->
![Data Science Hierarchy of Needs](https://hackernoon.com/hn-images/1*7IMev5xslc9FLxr9hHhpFw.png){:height="400px"}

There is an excellent [article](https://hackernoon.com/the-ai-hierarchy-of-needs-18f111fcc007) by Monica Rogati talking about how you set up a good foundation for your data before going for AI/Machine Learning.

## The Full Stack Data Scientist

From data collection to the creation of Deep/Machine Learning models, the data scinece process entails a variety of work to be performed, illustrated as tiers in this pyramid. A person who does all the work across the spectrum, can be called a **Full Stack Data Scientist**. 

Considered rare and sometimes referred to as Unicorn Data Scientists, Full Stack Data Scientists can be found in startups and nascent small firms who cannot hire specialized resources for each tier due to resource constraints. However, such candidates can be quite rare, and can be a bit on the expensive side, so it's not pragmatic for any firm to just be hiring Full Stack Data Scientists. Besides, none of the candidates I mentioned above meet the criteria of a Full Stack Data Scientist, so lets break down the tiers into roles.

## Roles in a Data Science team

- **Data Engineer**
Operating at the tier 1 & 2 of the pyramid, Data Engineers are responsible for collecting data from sources, getting it onto the firm's storage and compute infrastructure. They will be skilled in performing ETL (Extract, Transform, Load) and ELT (Extract, Load, Transform), and will be the ones maintaining the data lake and data warehouse, using big data tools to create and manage data pipelines. Their technology stack includes data ingestion tools (batch and streaming), distributed storage and processing (hadoop family of tools), structured and unstructure storage technologies (Cassandra, MongoDB, Vertica, etc.), as well as some data orchestration frameworks (Apache Airflow, Nifi, etc.)

- **Data Analyst**
A Data Analyst utilized business acumen and analytical skills to bridge the gap between the purely technical Data Science teams and the business units. The business expertise also makes the Data Analyst quite a key role in helping establishing business needs. Data Analysts will use the data provided to them, and figure out the best way to transform it into information which can improve the business. They will be skilled in data interpretation and analysis, and building useful reports and dashboards which business can readily use to improve or track their KPIs. A Data Analyst can be mapped roughly on tier 4 of the data hierarchy of needs.

- **Data Scientist**
The Data Scientist's role is in solving business problems using a mixture of mathematics, statistics and machine learning. Data Scientists' skills will fall on the data tiers above tier 3 on the pyramid. The Data Scientist is quite proficient in selecting the data science technique given the business problem at hand and creating the right models for them. Data Scientists are quite adept with statistical analyses and techniques, including experiment design and A/B testing. They work with diverse problems across different data domains to find and develop solutions for functional problems across the organization, and are proficient with core principles & modern tooling in data science, including machine learning (eg sklearn, Pytorch, Tensorflow), data and text analytics, clustering analysis, pattern recognition and extraction, automated classification and categorization. 

- **Machine Learning Engineer**
The Machine Learning Engineer's job in a Data Science team is to take the models that the Data Scientist has built and validated, and functionalize them. This includes end-to-end implementation and operationalization of ML use cases, staying mindful of scalable data engineering and Machine Learning pipelines. Their job is to find the best way to deploy the ML models on the available infrastructure to keep it scalable and fault-tolerant, as well as serve real-time and batch ML pipelines. They also write code to retrain and keep the models updated, using hyperparameter tuning techniques to optimize the models, while monitoring the production environment for data drift. They fall on the same tiers as the Data Scientists, but look to productionization needs more than innovative problem solving needs.

## The disconnect in the status quo
Mapping the skills of the three candidates to the Data Science hierarchy of needs, I can easily see that A is a Data Scientist, B could be a Machine Learning Engineer, and C could easily qualify for a Data Analyst. And all 3 of them had shown up for a Data Scientist vacancy. From my requirements, our recruitment also made a mistake advertising a job-opening for a "Data Scientist" when we should have advertised a job opening for a "Machine Learning Engineer".

The problem with the industry is that a lot of people are still unaware of the differences in skills that set apart these roles. Recruiters and applicants alike are still illusioned by the title of "Data Scientist", framing a two fold problem:

- Recruiters would advertise job openings with a generic title of "Data Scientist" but ask for skills across the spectrum. It appears they are looking for the unicorn Data Scientist, when they just need an Analyst or a ML Engineer if they understood their own needs.

- Applicants, on the other hand, instead of recognizing their own strengths and playing to them, try to assume the title of Data Scientist.

The result is an immature market with a disillusionment and disappointment on both the employer and employee ends.

## A capable Data Science team
A good team would be diversified across all the pyramid tiers and have a strong balance of skills required to take an idea from POC to production. An employer can do this by trying to hire jack-of-all-trades, or, specialized skills could be identified and hired for. 

As an employer, you should try to identify exactly what it is that you need to hire for. If it's not a multidisciplinary full-stack data scientist that you need, you should not have to pay a premium for buying a light-saber when a pocket knife could do the job.

<span style="font-size:16px;color:grey;">Photo by <a href="https://unsplash.com/@campaign_creators?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText">Campaign Creators</a> on <a href="https://unsplash.com/s/photos/data?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText">Unsplash</a></span>