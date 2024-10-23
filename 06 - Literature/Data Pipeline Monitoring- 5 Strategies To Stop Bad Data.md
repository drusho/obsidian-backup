---
title: Data Pipeline Monitoring- 5 Strategies To Stop Bad Data
source: https://www.montecarlodata.com/blog-data-pipeline-monitoring/
author:
  - "Barr Moses"
published: 2024-02-01T20:22:00-08:00
description: Here are three data pipeline monitoring strategies the best data teams are leveraging to detect and prevent bad data from corrupting their pipelines.
tags:
  - data
  - pipeline
  - engineering
---
For data teams, bad data, broken data pipelines, stale dashboards, and 5 a.m. fire drills are par for the course, particularly as [data workflows](https://www.montecarlodata.com/blog-the-art-of-data-workflows-a-step-by-step-guide/) ingest more and more data from disparate sources. That’s where data pipeline monitoring comes in.

So, what are data pipeline monitoring tools and how can they help you detect, resolve, and prevent bad data?

In this article, I share the five key data pipeline monitoring strategies some of the best data organizations in the industry are leveraging to restore trust in their data—as well as the tools and metrics you can use to help you get started faster.

## Table of Contents

- [What is data pipeline monitoring?](https://www.montecarlodata.com/blog-data-pipeline-monitoring/#what-is-data-pipeline-monitoring)
- [1\. Ensure your data pipeline monitoring covers unknown unknowns](https://www.montecarlodata.com/blog-data-pipeline-monitoring/#1-ensure-your-data-pipeline-monitoring-covers-unknown-unknowns)
- [2\. Monitor broadly across your production tables and end-to-end across your data stack](https://www.montecarlodata.com/blog-data-pipeline-monitoring/#2-monitor-broadly-across-your-production-tables-and-end-to-end-across-your-data-stack)
- [3\. Combine monitoring with data testing](https://www.montecarlodata.com/blog-data-pipeline-monitoring/#3-combine-monitoring-with-data-testing)
- [4\. Understand data lineage and downstream impacts](https://www.montecarlodata.com/blog-data-pipeline-monitoring/#4-understand-data-lineage-and-downstream-impacts)
- [5\. Make metadata a priority, and treat it like one](https://www.montecarlodata.com/blog-data-pipeline-monitoring/#5-make-metadata-a-priority-and-treat-it-like-one)
- [Data Pipeline Monitoring Tools](https://www.montecarlodata.com/blog-data-pipeline-monitoring/#data-pipeline-monitoring-tools)
- [Data observability:](https://www.montecarlodata.com/blog-data-pipeline-monitoring/#data-observability)
- [Data quality testing:](https://www.montecarlodata.com/blog-data-pipeline-monitoring/#data-quality-testing)
- [Data contracts:](https://www.montecarlodata.com/blog-data-pipeline-monitoring/#data-contracts)
- [Data pipeline monitoring dashboard:](https://www.montecarlodata.com/blog-data-pipeline-monitoring/#data-pipeline-monitoring-dashboard)
- [Data Pipeline Monitoring Metrics](https://www.montecarlodata.com/blog-data-pipeline-monitoring/#data-pipeline-monitoring-metrics)
- [The Future of Bad Data and Data Downtime](https://www.montecarlodata.com/blog-data-pipeline-monitoring/#the-future-of-bad-data-and-data-downtime)

Data pipeline monitoring is the process of leveraging [data quality tools](https://www.montecarlodata.com/blog-data-quality-tools-when-you-need-them/) like data observability to gain visibility into the health of your data and its fitness for a given use-case.

The way this is most often framed is simply, “How do we catch bad data” 

I once spoke with a data leader whose team was responsible for serving terabytes of data to hundreds of stakeholders per day. Given the scale and speed at which they were moving, poor data quality was an all-too-common occurrence. At Monte Carlo, we call this [data downtime](https://www.montecarlodata.com/blog-the-rise-of-data-downtime/)—periods of time when data is fully or partially missing, erroneous, or otherwise inaccurate. 

How many times have you had a stakeholder in marketing (or operations or sales or any other business function that uses data) notice that the metrics in their dashboard look off and reach out to alert your team, only to have your team stop what they’re doing to troubleshoot.Any time this happens, it almost invariably results in **lost trust**, **lost time,** and **lost opportunities** to create new value for your stakeholders.

The idea of preventing bad data is standard practice across many industries that rely on functioning systems to run their business, from preventative maintenance in manufacturing to error monitoring in software engineering (queue the dreaded 404 page…).

Yet, many of the same companies that tout their data-driven credentials aren’t investing in data pipeline monitoring to detect bad data before it moves downstream. Instead of being proactive about data downtime, they’re [reactive](https://www.datacouncil.ai/talks/introducing-data-downtime-from-firefighting-to-winning), playing whack-a-mole with bad data instead of focusing on preventing it in the first place.

Fortunately, there’s hope. Some of the most forward-thinking data teams have developed best practices for preventing data downtime and stopping broken pipelines and inaccurate dashboards in their tracks, before your CEO has a chance to ask the dreaded question: “what happened here?!”

**Now, let’s take a look at five key data pipeline monitoring strategies you can use to prevent bad data from corrupting your otherwise good pipelines**:

### 1\. Ensure your data pipeline monitoring covers unknown unknowns

Data testing–whether hardcoded, [dbt tests](https://www.montecarlodata.com/blog-dbt-unit-testing-mistakes/), or other types of unit tests–has been the primary mechanism to improve data quality for many data teams.

The problem is that you [can’t write a test anticipating every single way data can break](https://www.montecarlodata.com/blog-data-observability-vs-data-testing-everything-you-need-to-know/), and even if you could, that can’t scale across every pipeline your data team supports. I’ve seen teams with more than a hundred tests on a single data pipeline throw their hands up in frustration as bad data still finds a way in.

Hyper scalable ML-based monitoring tools like those found in Data Observability allow you to quickly scale coverage for unknown-unkowns across your data environment to

### 2\. Monitor broadly across your production tables and end-to-end across your data stack

Data pipeline monitoring must be powered by machine learning metamonitors that can understand the way your data pipelines typically behave, and then send alerts when anomalies in the data freshness, volume (row count), or schema occur. This should happen [automatically and broadly across all of your tables](https://www.montecarlodata.com/blog-data-anomaly-and-quality-monitoring/) the minute they are created.

It should also be paired with machine learning monitors that can understand when anomalies occur in the data itself–things like NULL rates, percent uniques, or value distribution.

### 3\. Combine monitoring with data testing

![Illustration of testing and monitoring being combined as part of data pipeline monitoring. ](https://www.montecarlodata.com/wp-content/uploads/2024/02/Data-Pipeline-Monitoring-1024x768.webp)

*For most data teams, testing is the first line of defense against bad data.*

Automated ML-based monitoring is a must, but data testing is table stakes (no pun intended).

In the same way that software engineers unit test their code, [data testing](https://www.montecarlodata.com/blog-data-observability-vs-data-testing-everything-you-need-to-know/) helps data teams validate their data and code across every stage of their data pipelines.

Schema tests and custom-fixed data tests are both common methods, and can help confirm your data pipelines are working correctly in expected scenarios. These tests look for warning signs like null values and referential integrity, and allows you to set manual thresholds and identify outliers that may indicate a problem. When applied programmatically across every stage of your pipeline, data testing can help you detect and identify issues before they become data disasters.

Data testing supplements data pipeline monitoring in two key ways. The first is by setting more granular thresholds or data SLAs. If data is loaded into your data warehouse a few minutes late that might not be anomalous, but it may be critical to the executive who accesses their dashboard at 8:00 am every day.

The second is by stopping bad data in its tracks before it ever enters the data warehouse in the first place. This can be done through data circuit breakers using the [Airflow ShortCircuitOperator](https://www.montecarlodata.com/blog-airflow-shortcircuitoperator-data-circuit-breaker/), but caveat emptor, with great power comes great responsibility. You want to reserve this capability for the most well defined tests on the most high value operations, otherwise it may add rather than remove your data downtime.

### 4\. Understand data lineage and downstream impacts

![](https://www.montecarlodata.com/wp-content/uploads/2023/11/automated-lineage-tracing.png)

*Field and table-level lineage can help data engineers and analysts understand which teams are using data assets affected by data incidents upstream. Image courtesy of Barr Moses.*

Often, bad data is the unintended consequence of an innocent change, far upstream from an end consumer relying on a data asset that no member of the data team was even aware of. This is a direct result of having your data pipeline monitoring solution separated from [data lineage](https://www.montecarlodata.com/blog-data-lineage/) — I’ve called it the **[“You’re Using THAT Table?!”](https://www.montecarlodata.com/blog-the-rise-of-data-downtime/)** problem.

Data lineage, simply put, is the end-to-end mapping of upstream and downstream dependencies of your data, from [ingestion](https://www.montecarlodata.com/blog-data-ingestion/) to analytics. Data lineage empowers data teams to understand every dependency, including which reports and dashboards rely on which data sources, and what specific transformations and modeling take place at every stage.

When data lineage is incorporated into your data pipeline monitoring strategy, especially at the field and table level, all potential impacts of any changes can be forecasted and communicated to users at every stage of the data lifecycle to offset any unexpected impacts.

While downstream lineage and its associated business use cases are important, don’t neglect understanding which data scientists or engineers are accessing data at the warehouse and lake levels, too. Pushing a change without their knowledge could disrupt time-intensive modeling projects or infrastructure development.

### 5\. Make metadata a priority, and treat it like one

![When applied to a specific use case, metadata can be a powerful tool for bad data incident resolution.](https://cdn-images-1.medium.com/max/1600/1*jheLmR5CN5ge1jLqh7u8ag.png)

*When applied to a specific data pipeline monitoring use case, metadata can be a powerful tool for data incident resolution. Image courtesy of Barr Moses.*

Lineage and metadata go hand-in-hand when it comes to data pipeline monitoring and preventing data downtime. Tagging data as part of your lineage practice allows you to specify how the data is being used and by whom, reducing the likelihood of misapplied or broken data.

Until all too recently, however, metadata was treated like those empty Amazon boxes you SWEAR you’re going to use one day — hoarded and soon forgotten.

As companies invest in more data solutions like [data observability](https://www.montecarlodata.com/blog-what-is-data-observability/), more and more organizations are realizing that metadata serves as a seamless connection point throughout your increasingly complex tech stack, ensuring your data is reliable and up-to-date across every solution and stage of the pipeline. Metadata is specifically crucial to not just understanding which consumers are affected by data downtime, but also informing how data assets are connected so data engineers can more collaboratively and quickly resolve incidents should they occur.

When [metadata is applied according to business applications](https://www.montecarlodata.com/blog-data-teams-your-metadata-is-useless/), you unlock a powerful understanding of how your data drives insights and decision making for the rest of your company.

There are several critical data pipeline monitoring tools that support data quality. What you choose and how complex your data pipeline monitoring tools and infrastructure will be will depend largely on the scale of your data platform and the needs of your data team, but these three are a good place to start.

### **Data observability**:

You can think of data observability as the bread and butter of your data pipeline monitoring. Data observability leverages metadata to provide a broad low-compute layer of coverage across your entire pipeline so you can quickly monitor your pipelines end-to-end. Unlike traditional manual data pipeline monitoring, data observability leverages machine learning to automatically create monitors, set thresholds, and define the lineage of your pipelines.

For complex and scaling data pipeline needs, data observability is a must.

### **Data quality testing**:

Custom testing like [dbt tests](https://docs.getdbt.com/docs/build/tests) or Monte Carlo’s Custom Monitors provides additional “deep” coverage for your most critical tables by querying your data directly. This naturally provides a greater level of quality coverage but at a greater compute cost, which is why this type of data pipeline monitoring should always be reserved for where it will provide the most impact for your downstream consumers.

### **Data contracts**:

While not directly a data pipeline monitoring tool, [data contracts](https://www.montecarlodata.com/blog-data-contracts-explained/) help data teams prevent data quality issues that arise from unexpected schema changes and data swamps.

More often than not, the software engineers in charge of the systems and services that create production data aren’t the same teams tasked with maintaining them and might be unaware of the data dependencies involved. So, if a software engineer makes an update that results in a schema change, and the data engineers aren’t aware, you’ve got yourself a broken pipeline.

Much like an SLA in software engineering, data contracts are merely a formalized a process—sometimes relying on specific technologies—to help data producers and data consumers set and enforce standards and expectations.

### Data pipeline monitoring dashboard:

While not a data pipeline monitoring tool in and of itself, a data pipeline monitoring dashboard can go a long way towards helping teams visualize and understand the health of their data pipelines.

![This Monte Carlo dashboard is an example of a data pipeline dashboard.](https://www.montecarlodata.com/wp-content/uploads/2024/03/Untitled-design.gif)

Additional tools like Monte Carlo’s data health dashboards help data teams see at a glance how their data is performing in aggregate against data quality metrics and gives them the power to quickly drill down into trouble spots for a deeper look.

![monte carlo reliability dashboard data quality tools](https://www.montecarlodata.com/wp-content/uploads/2024/01/monte-carlo-reliability-dashboard-1-1024x646.png)

## Data Pipeline Monitoring Metrics

Because data observability is designed to provide end-to-end coverage across a data pipeline, the 5 pillars of data observability are also—not coincidentally—the best metrics to employ for monitoring your data pipelines. Those metrics include:

1\. Freshness  
2\. Quality  
3\. Volume  
4\. Schema  
5\. Lineage

By leveraging these five pillars, you can maintain a comprehensive understanding of the health of your pipelines as well as where breaks are happening and how to quickly resolve issues before they can impact downstream user.

## The Future of Bad Data and Data Downtime

![End-to-end lineage powered by metadata gives you the necessary information to not just troubleshoot bad data and broken pipelines, but also understand the business applications of your data at every stage in its life cycle. Image courtesy of Barr Moses.](https://www.montecarlodata.com/wp-content/uploads/2021/01/0_WabTxw4WnGmu_0Z-1-1-1024x611.png)

End-to-end lineage powered by metadata gives you the necessary information to not just troubleshoot bad data and broken pipelines, but also understand the business applications of your data at every stage in its life cycle. Image courtesy of Barr Moses.

So, where does this leave us when it comes to realizing our dream of a world of data pipeline monitoring that ends data downtime?

Well, like death and taxes, data errors are unavoidable. But when metadata is prioritized, lineage is understood, and both are mapped to testing and data pipeline monitoring, the negative impacts on your business — [the true cost of bad data and data downtime](https://www.montecarlodata.com/blog-the-rise-of-data-downtime/) — is largely preventable.

I’m predicting that the future of broken data pipelines and data downtime is dark. And that’s a good thing. The more we can prevent data downtime from causing headaches and fire drills, the more our data teams can focus on projects that drive results and move the business forward with trusted, reliable, and powerful data.

***Have some data downtime stories to share? Interested in data pipeline monitoring? I’m all ears. Book a time to speak with us using the form below.***

Our promise: we will show you the product.