---
title: Process Mining architecture
description: Understand the basic attributes of the Process Mining architecture.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/process-mining/process-mining-architecture.html
release: zurich
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring Process Mining, Process Mining, Platform Analytics]
---

# Process Mining architecture

Understand the basic attributes of the Process Mining architecture.

-   The Process Mining mining engine extracts data from the audit history based on the project settings. The data file is then uploaded to a centralized training server \([ServiceNow® Predictive Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/predictive-intelligence/predictive-intelligence.md)\) within the same datacenter. The centralized training server enables advanced computing of new metrics. The centralized server supports more data for scalability without causing any performance load on your instance.
-   When the Process Mining project is ready, the training server sends the final project back to your instance and deletes all of your project data from the server. The data is transferred using secured and encrypted APIs.
-   The most recent version of the project is then visualized through the Analyst workbench UI on your instance.

\[Omitted image "process-optimization-architecture.png"\] Alt text: Process Mining architecture

**Parent Topic:**[Configuring Process Mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/process-mining/setting-up-process-mining.md)

**Related topics**  


[Predictive Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/predictive-intelligence/predictive-intelligence.md)

