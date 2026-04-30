---
title: Process Mining architecture
description: Understand the basic attributes of the Process Mining architecture.
locale: en-US
release: xanadu
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Process Mining, Process Mining, Platform Analytics]
---

# Process Mining architecture

Understand the basic attributes of the Process Mining architecture.

-   The Process Mining mining engine extracts data from the audit history based on the project settings. The data file is then uploaded to a centralized training server \([ServiceNow® Predictive Intelligence](https://www.servicenow.com/docs/access?context=predictive-intelligence&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)\) within the same datacenter. The centralized training server enables advanced computing of new metrics. The centralized server supports more data for scalability without causing any performance load on your instance.
-   When the Process Mining project is ready, the training server sends the final project back to your instance and deletes all of your project data from the server. The data is transferred using secured and encrypted APIs.
-   The most recent version of the project is then visualized through the Analyst Workbench UI on your instance.

![Process Mining architecture](../image/process-optimization-architecture.png)

**Parent Topic:**[Configuring Process Mining](setting-up-process-mining.md)

**Related topics**  


[Predictive Intelligence](https://www.servicenow.com/docs/access?context=predictive-intelligence&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)

