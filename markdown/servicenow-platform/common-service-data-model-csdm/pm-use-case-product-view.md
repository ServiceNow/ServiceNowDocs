---
title: Problem Management product view
description: Problem Management helps identify the cause of an error in the IT infrastructure, reported as occurrences of related incidents. The goal of this product view is to help you to understand how Problem Management key entities work with the core CSDM framework.
locale: en-US
release: xanadu
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Applying CSDM guidelines to your product, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Problem Management product view

Problem Management helps identify the cause of an error in the IT infrastructure, reported as occurrences of related incidents. The goal of this product view is to help you to understand how Problem Management key entities work with the core CSDM framework.

With Problem Management you can perform the following actions:

-   Document the root cause of an error and resolve it permanently.
-   Create known error articles from a problem to provide guidance and help deflect incidents.
-   Collaborate on problem tasks with other teams to identify the root cause using a drag-and-drop functionality on visual task boards.

The Problem Management form references the following CSDM elements \(attributes and related views\).

1.  Service — References the \[cmdb\_ci\_service\_business\] table.

    **Note:** Earlier releases labeled this attribute **Business Service**.

2.  Service Offering — References the \[service\_offering\] table to see the service offerings affected by the problem in the Service Offerings related list \[task\_service\_offering\].
3.  Configuration Items — References the \[cmdb\_ci\] table
4.  Affected/Causal CIs — Related list \[task\_ci\] table
5.  Impacted Services — Related list \[task\_cmdb\_ci\_service\] table

![Problem Management form with numbered fields.](../image/prob-mang-form.png "Change Request form")

-   **[Applying CSDM guidelines to Problem Management](../reference/pm-use-case.md)**  
Problem Management manages and uses CSDM tables. Several ServiceNow products benefit from and add value to Problem Management.
-   **[Problem Management use case](pm-use-case-example.md)**  
The Problem Management use case is described in this section.
-   **[Problem Management considerations](pm-use-case-trouble.md)**  
Consider these points while implementing the CSDM framework.

**Parent Topic:**[Applying the CSDM guidelines to your product](../reference/use-cases.md)

