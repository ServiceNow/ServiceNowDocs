---
title: Create an application service for unmapped servers
description: Maximize the use of your organization's resources by mapping application service candidates that include unmapped servers. Use the Service Mapping workspace's unmapped servers widget to create an application service and ensure that your servers are used efficiently.
locale: en-US
release: xanadu
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
keywords: [Service Mapping, Application Service, unmapped server, Service Mapping workspace]
breadcrumb: [Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Create an application service for unmapped servers

Maximize the use of your organization's resources by mapping application service candidates that include unmapped servers. Use the Service Mapping workspace's unmapped servers widget to create an application service and ensure that your servers are used efficiently.

## Before you begin

-   Ensure that Predictive Intelligence is enabled.
-   Verify Machine Learning readiness.
-   Confirm that the data is trained.

For more information, see [Application service readiness dashboard in configurable workspace](../reference/readiness-dashboard-ml.md)

**Important:**

Service Mapping Plus v.1.10.0 or higher:

To successfully update your data and view application candidates for unmapped servers, see [Troubleshooting steps for Mapping unmapped servers with Application service candidates \[KB1585065\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1585065) in the Now Support Knowledge Base.

Role required: service\_mapping\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Mapping**.

2.  Choose the unmapped server you want to create application service for.

    1.  In the **Unmapped servers** tile, select the **Unmapped Servers with Candidate ID** graph.

    2.  In the Unmapped servers with candidate list, review the list of suggested candidates.

        You can group by candidate IDs or by the servers to prioritize your work by right-clicking the relevant column name and selecting **Group By**.

    3.  Select the preferred candidate.

3.  Select **Map application service**.


## Result

The selected application service candidate is converted to an application service, and the selected unmapped servers are mapped.

**Parent Topic:**[Using Service Mapping](../concept/using-service-mapping.md)

