---
title: Applying CSDM guidelines to Change Management
description: Change Management lets you control every aspect of the IT change process from creation to approval. When you have accurate information, you can minimize risks to your business and avoid conflicts with scheduling. The goal of this product view is to help you to understand how Change Management key entities work with the core CSDM framework.
locale: en-US
release: xanadu
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure, Change Management, IT Service Management]
---

# Applying CSDM guidelines to Change Management

Change Management lets you control every aspect of the IT change process from creation to approval. When you have accurate information, you can minimize risks to your business and avoid conflicts with scheduling. The goal of this product view is to help you to understand how Change Management key entities work with the core CSDM framework.

## Change Management

Change Management includes the following features:

-   Manage changes more quickly by using the Change Advisory Board \(CAB\) Workbench to schedule, plan, and manage CAB meetings from one interface.
-   The Change Management backlog analysis dashboard provides increased visibility into any changes.
-   Service Maps let you see the change impacts at-a-glance.
-   The change approval policies increase DevOps velocity and remove IT friction.

For details on implementing the CSDM framework, see [Implementing the CSDM framework in stages](https://www.servicenow.com/docs/access?context=csdm-implementation-stages&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

## Change Request form

The Change Request form references the following attributes and related lists.

<table id="table_rsk_l4b_1wb"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

1 Service \(Business Service\)

</td><td>

References the \[cmdb\_ci\_service\_business\] table.

 **Note:** Earlier platform releases labeled this attribute **Business Service**.

</td></tr><tr><td>

2 Service Offering

</td><td>

References the \[service\_offering\] table where the offering has a parent service.

</td></tr><tr><td>

3 Configuration Items

</td><td>

References the \[cmdb\_ci\] table.

</td></tr><tr><td>

4 Affected/Causal CIs

</td><td>

Related list \[task\_ci\] table.

</td></tr><tr><td>

5 Impacted Services

</td><td>

Related list \[task\_cmdb\_ci\_service\] table.

</td></tr><tr><td>

6 Assignment Group

</td><td>

References the Group attribute.**Note:** You can populate the Group attribute by using the Assignment Group for the relevant CI.

</td></tr></tbody>
</table>![Change Request form with numbered fields.](../image/itsm-change-form.png)

## For more information

For additional details on Change Management, see [Change Management](c_ITILChangeManagement.md).

[See the video: How Change Management leverages the CSDM](https://www.youtube.com/watch?v=3iCxTeU4ZTA&list=PLkGSnjw5y2U7QNr9jL6TAgwQvYBI_LEtK&index=43)

-   **[Change Management and CSDM tables](../reference/itsm-change-use-case.md)**  
Change Management manages and uses CSDM tables. Several ServiceNow products benefit from and add value to Change Management.
-   **[Change Management use case](itsm-change-use-case-example.md)**  
For ITSM, specifically incident and change, identifying the location of critical data can help reduce mean time to resolve incidents and eliminate outages caused by change.
-   **[Change Management considerations](itsm-change-use-case-trouble.md)**  
Consider these points while implementing the CSDM framework.

**Parent Topic:**[Configuring Change Management](configure-change-management.md)

