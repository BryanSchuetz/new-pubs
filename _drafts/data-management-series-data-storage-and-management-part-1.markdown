---
title: 'Data Management Series: Data Storage and Management (Part 2)'
date: 2017-08-31 13:51:00 -04:00
tags:
- Data Visualization
- Data
- Data Management Series
Author: "[Ben Mann](https://www.dai.com/who-we-are/our-team/ben-mann); [Karim Bin-Humam](https://www.dai.com/who-we-are/our-team/karim-bin-humam)"
---

*This is the second post in a series on data management. You can read part one [here](dai-global-digital.com/data-management-series-planning-and-collecting-part-1.html)*

So, after reading [last week's blog](dai-global-digital.com/data-management-series-planning-and-collecting-part-1.html), you've developed the world's most robust Monitoring, Evaluation, and Learning plan. You just conducted a multi-tier baseline assessment, validating your data by triangulating data points through five different surveying tools and are excited to dig in to multivariate regression analysis. But wait! First we need to talk about data storage and management!

In the international development world, binders full of data (disaggregated by gender of course) on shelves in rural government offices are as common place as smiling children splashing in the crystal clear water of a newly constructed well. We all acknowledge that there are much better ways to store and maintain our results. However, many organizations only move one or two steps up the ladder: from paper and pen to Excel or CSV files on an office laptop. While this may enable you to conduct the minimum analysis needed to satiate your donor in an annual report, does it really maximize the value of the data we collect?

![r4dSkills_DataManagement.png](/uploads/r4dSkills_DataManagement.png)
<!--more-->

Along the Data Management Chain, all links are equal in importance. However, storage is often the weakest by far. Revisiting our commodity analogy from the first post in this series: would you rather put all of your oil in an array of small, paper cups with lots of holes or a large steel barrel with reinforced sides? A good data storage and management plan should enable you to do the following things:

* Store your data, without a fear of loss

* Map your data model, without inaccurate or inconsistent relationships

* Clean your data, without risk of versioning mishaps

* Secure your data, without compromising flexibility

* At DAI, we ensure that the systems we use to store and manage our data fulfill all of these criteria.

When it comes to storage, the following considerations are essential when designing a broader data management system:

**Hosting: Local vs. Cloud:**

One of the first decisions that has to be made regarding data storage is whether data is to be stored on local servers or on the cloud. Generally speaking, cloud storage tends to be more cost effective, requiring less up-front costs for equipment. It also requires less maintenance effort (or none at all) as all updates and security patches are handled by the service provider and are included in the cost of service. The cloud also offers major advantages for scalability (purchasing more storage space is simple) and security, as cloud storage providers often employ advanced, industry standard security protocols, and data is automatically backed up in the cloud. On the other hand, local storage offers the advantage of speed and uptime for projects working with poor internet infrastructure. Cloud storage certainly carries a lot of advantages, but the choice may be made for you if reliable cloud services aren’t offered in your locale.

**Database Types:**

Ok so you know where you want to store your data, you should be all set to upload your data and get started with regression analysis, right? Wrong. You also have to consider what type of database you will be using since there are many. The main distinction here is between relational and non-relational databases. SQL and Oracle are relational databases and are characterized by multiple data ‘buckets’ that are linked to one another by relationships that require a link or a ‘key’. Non-relational databases such as MongoDB on the other hand store data without explicit structures and mechanisms to link data between buckets. While the pros and cons of both are many, this choice typically boils down to the fact that relational DBs make it easy to structure and combine datasets, but do not scale horizontally as well as non relational BDs.

![7e26d5c20f89e7dc217d3d83a1d89e06.jpg](/uploads/7e26d5c20f89e7dc217d3d83a1d89e06.jpg)`Relational (SQL) vs. Non Relational (NoSQL) databases, photo credit: [PACHOSTING Platform Aggregated Cloud](https://www.pachosting.hk/en/)`

**Cleaning:**

Anyone we know that has ever worked with moderately large datasets will almost certainly tell you the same thing if you were to ask them what aspect of their work is the most time-intensive. “Don’t underestimate the time it takes to clean data” they are likely to say. Maybe you’ll get lucky – maybe the people collecting the data your organization work with advanced collection tools and make no data entry errors such as spelling mistakes, or using a number in place of a text, or enter GPS coordinates of 0 instead of none at all for a data point without a location (you would be surprised to see how many schools appear to be located in the Atlantic Ocean off the coast of Ghana). As is the case for all categories, a number of tools both manual and algorithmic exist that can support you in removing duplicates, reformatting data points, and correcting incorrect data. The tools that we use enable us to perform relatively complicated cleaning or “scrubbing” without needing to have advanced programming skills.

**Security:**

Encompassing all of the categories above, any data management plan must account for security. This means server-side security to ensure that no one can access your data without permission. It means internal personal account security, for your system users and data subjects, so their personally identifiable information doesn’t leak into the wrong hands accidentally. There are many tools and approaches to tackle these issues, from data masking and user levels to high level, end-to-end encryption. One of the worst outcomes of any data management plan is compromised data from a malicious source—our plans always account for the resource costs needed to keep our systems and data safe and secure.

Data storage and maintenance can be the most complex element of the data management chain. Beyond these first categories lie a myriad of other considerations that should be planned for at the beginning and will influence your choices for database structures. For a deeper look at these important topics, check out these resources:

* [ACID vs. BASE](https://neo4j.com/blog/acid-vs-base-consistency-models-explained/)

* [Creating a Data Model](http://www.bridging-the-gap.com/data-model-not-too-technical/)

* [What is ETL and why does it matter?](https://www.sas.com/en_my/insights/data-management/what-is-etl.html)