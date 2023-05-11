---
layout: post
title:  "My experience with Google's Recommender AI service"
subtitle: "Why a powerful technology's adoption hindered"
date:   2022-08-08 12:02:00 +0500
background: '/img/posts/googrecai.png'
---

Google's Recommender AI service is a powerful tool that can help businesses personalize their online content, products, and services to meet the unique needs of their customers. This technology uses machine learning algorithms to analyze customer data and make recommendations based on their preferences, behavior, and demographics. While there are many benefits to using Google's Recommender AI service, there are also some potential drawbacks to consider. In this article, I will share my experience with using RecAI, and discuss why we decided not to adopt it.

I worked with Recommender AI during my time at eBay, starting with the most basic POC. We took an opensource retail dataset, threw it at RecAI, and voila! It gave some qualitatively good recommendations. At first glance, it was too good... 
- the GCP portal offered a UI
- a Python API was available
- the service was scalable, and could be integrated with BigQuery to handle large scale data
- real-time recommendations could be served out of an API

However, when we started working on eBay's proprietary data, and ran POCs on that, certain fallbacks started to surface.
#### A blackbox model
The RecAI service was a complete blackbox model. Though it offered different types of recommendation scenarios for modeling (seedless vs seeded recommendations, more like this, recommended for you, etc.), we had no idea about the model architecture behind the scenes. And that's not entirely a dealbreaker, sure... BUT...

#### An utter lack of evaluation metrics
We also didn't have any way of knowing how good/bad the trained model was (after 5 days of training time). There weren't any metrics like recall@topK, or even something as fundamental as a MSE error metric. If we needed such evaluations over proprietary datasets, we needed to write a framework to keep a holdout set OUTSIDE of RecAI, and create evaluations by first taking recommendations from the trained model via API. VERY expensive! Both computationally, and dev-time wise.

#### The validation supported by RecAI
RecAI did offer A/B testing of live traffic, but considering how time-consuming and complicated it could be to first do production level integration with the service, only to find out that your proprietary models beat the service, is NOT worth it! It takes a whole team and 3-4 months to integrate the system end-to-end, and that's a whole investment that doesn't make sense for just evaluating if you created a good model or not.

#### Batch event ingestion delays
Having prepared the dataset in the required format, and made it available in BigQuery on GCP, there was still a delay of a few hours before the data updated inside the RecAI service. So if you want to do quick experimentation, you'll need to wait after the data is at the target, just so that the service could update its catalog.

#### Room for experimentation
If we wanted to have multiple versions of catalogs (a catalog is a combination of items and events), we'd need to set up difference GCP projects. It is absolutely not possible to create multiple catalogs within one project. If you're working in an organization where creating a new project, and setting up permissions for the developers comes with a red-tape, you'll hate it. I needed different models for different regions, so their catalogs had to be separate, and that was certainly not an enjoyable aspect.

#### Difficulty with API
As much as I was happy to know that there was a Python API available to use with RecAI, it turned out to be VERY hard to use. The documentation had little description of classes/objects/methods, and I had to infer a lot just to use it. Also, the API expected us to work with API objects to provide simple configurations, where they could have simply gotten around that by just using a JSON. All in all, it was not a friendly experience writing code for the RecAI API.

So, all things considered, we gave appropriate feedback to the product team at Google, and killed the project. For a company as big as eBay, the technology isn't mature enough as of this day. Maybe in a few years' time, the team will give it a go again.