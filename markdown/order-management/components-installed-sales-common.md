---
title: Components installed with Sales Common
description: Several types of components are installed with activation of the Sales Common \(sn\_sales\_common\) plugin, including user roles and tables.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/components-installed-sales-common.html
release: australia
topic_type: reference
last_updated: "2026-08-10"
reading_time_minutes: 1
breadcrumb: [Sales automation, Reference, Sales Customer Relationship Management]
---

# Components installed with Sales Common

Several types of components are installed with activation of the Sales Common \(sn\_sales\_common\) plugin, including user roles and tables.

## Roles installed

<table id="table_roles"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Sales manager

 \[sn\_sales\_common.sales\_manager\]

</td><td>

Assigns opportunities to sales agents based on the team's expertise and creates, reads, and updates opportunities.

</td><td>

sn\_sales\_common.sales\_agent

</td></tr><tr><td>

Sales agent

 \[sn\_sales\_common.sales\_agent\]

</td><td>

Creates, reads, and updates opportunities assigned by a sales manager to identify, nurture, and convert opportunities into successful sales.

</td><td>

-   sn\_quote\_mgmt\_core.quote\_writer
-   sn\_som\_gen\_ai.sales\_ai\_user
-   sn\_meeting\_mgmt.meeting\_creator
-   sn\_mcp\_server.viewer
-   sn\_crm\_touchpoint.touchpoint\_writer
-   sn\_sales\_forecast.forecast\_viewer
-   sn\_doc.reader
-   sn\_customerservice.csm\_workspace\_user
-   sn\_opty\_mgmt\_core.opportunity\_setup\_viewer
-   sn\_opty\_mgmt\_core.opportunity\_writer
-   sn\_opty\_mgmt\_core.opportunity\_allocation\_writer

</td></tr><tr><td>

Sales order specialist

 \[sn\_sales\_common.sales\_order\_specialist\]

</td><td>

Includes both the sales agent role and the order agent role access, so sales order specialists can work on both middle-office and front-office activities for creating quotes and orders within a company.

</td><td>

sn\_sales\_common.sales\_agent

</td></tr><tr><td>

Sales restricted agent

 \[sn\_sales\_common.sales\_restricted\_agent\]

</td><td>

Provides access to leads, opportunities, quotes, sales territories, and other resources, enabling the user to manage the sales life cycle effectively through the responsibility framework.

</td><td>

-   sn\_customerservice.cust\_data\_resp\_granular
-   sn\_opty\_mgmt\_core.opportunity\_setup\_viewer
-   sn\_customerservice.csm\_workspace\_user
-   sn\_crm\_touchpoint.touchpoint\_writer
-   sn\_mcp\_server.viewer
-   sn\_opty\_mgmt\_core.opportunity\_allocation\_responsibility\_write\_granular
-   sn\_meeting\_mgmt.meeting\_creator
-   sn\_crm\_customer\_access\_management\_user
-   sn\_quote\_mgmt\_core.quote\_responsibility\_write\_granular
-   sn\_prd\_pm.product\_catalog\_viewer
-   sn\_csm\_ctxrul\_mgt.context\_variable\_viewer
-   sn\_tmt\_core.inbound\_queue\_read
-   sn\_opty\_mgmt\_core.opportunity\_responsibility\_write\_granular
-   sn\_csm\_ctxrul\_mgt.rule\_matrix\_viewer

</td></tr><tr><td>

Sales operations specialist

 \[sn\_sales\_common.sales\_ops\_specialist\]

</td><td>

Configures and optimizes the sales process within an organization by handling administrative and setup tasks, ensuring that the sales team operates within a well-structured framework for tracking and managing sales transactions from initiation to closure.

</td><td>

-   sn\_som\_gen\_ai.sales\_ai\_admin
-   sn\_opty\_mgmt\_core.opportunity\_setup\_writer
-   canvas\_user
-   sn\_opty\_mgmt\_core.opportunity\_allocation\_viewer
-   sn\_doc.writer
-   sn\_crm\_touchpoint.touchpoint\_reader
-   sn\_quote\_mgmt\_core.quote\_viewer
-   sn\_opty\_mgmt\_core.opportunity\_viewer
-   sn\_sales\_forecast.forecast\_admin
-   sn\_meeting\_mgmt.meeting\_viewer

</td></tr></tbody>
</table>## Tables installed

<table id="table_tables"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Sales CRM Progression Checkpoint

 \[sn\_sales\_common\_sales\_crm\_progression\_checkpoint\]

</td><td>

Records that track progression checkpoint events for an object as it moves through the sales life cycle.

</td></tr></tbody>
</table>**Parent Topic:**[Sales automation reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/reference-lead-opportunity-mgt.md)

