---
title: Process Mining architecture
description: Understand the basic attributes of the Process Mining architecture.
locale: en-US
release: australia
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Explore, Process Mining, Platform Analytics]
---

# Process Mining architecture

Understand the basic attributes of the Process Mining architecture.

-   The mining engine of Process Mining extracts data from the audit history based on the project settings. The data file is then uploaded to a centralized training server \(ServiceNow® Predictive Intelligence\) within the same datacenter. The centralized training server enables advanced computing of new metrics. The centralized server supports more data for scalability without causing any performance load on your instance.
-   When the Process Mining project is ready, the training server sends the final project back to your instance and deletes all project data from the server. The data is transferred using secured and encrypted APIs.
-   The most recent version of the project is then visualized through the Analyst workbench UI on your instance.

For detailed information on data handling and security in Predictive Intelligence products, see [KB article KB1584480](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1584480).

![Process Mining architecture](../image/process-optimization-architecture.png)

**Parent Topic:**[Exploring Process Mining](explore-process-mining.md)

**Related topics**  


[Key features of Process Mining](key-features.md)

[Evaluation projects](evaluate-pm.md)

[Process Mining workspace](analyst-workbench-overview.md)

[bundle-platai.predictive-intelligence]

