---
title: Configuring filters for Manager Workspace
description: Configure filters for scheduling and coaching applications and use the default filter for channel management to refine your search results.
locale: en-US
release: xanadu
product: Workforce Optimization for Customer Service
classification: workforce-optimization-for-customer-service
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Workforce Optimization for Customer Service, Workforce Optimization for Customer Service, Customer Service Management]
---

# Configuring filters for Manager Workspace

Configure filters for scheduling and coaching applications and use the default filter for channel management to refine your search results.

## Before you begin

**Important:** Starting with the Tokyo release, Legacy Workforce Optimization is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Role required: sn\_csm\_wfo\_workspa.admin

## About this task

View and analyze data in scheduling and coaching applications based on the filters configured. You can only use the default filters for channel management and cannot configure new filters.

## Procedure

1.  Navigate to **All** &gt; **Workforce Optimization for Customer Service** &gt; **Manager Workspace Configuration** &gt; **Filter Configurations**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_xp1_hlt_jnb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Filter Name

</td><td>

Unique name for the filter configuration.

</td></tr><tr><td>

Table

</td><td>

Table for which the filter is configured. **Note:** You can filter only on specific tables or database views for each module.

Refer to Filter Configuration Tables in [Manager Workspace](../reference/components-installed-configurable-wfo-cs.md) for a list of tables and database views you can use for each application.

</td></tr><tr><td>

Field

</td><td>

Field on which to filter.

</td></tr><tr><td>

Filter Query

</td><td>

Query to narrow down the filter options.

</td></tr><tr><td>

Type

</td><td>

-   **Choice:** choice type field.
-   **Reference:** reference type field.


</td></tr><tr><td>

Order

</td><td>

Filter display order in Manager Workspace.

</td></tr><tr><td>

Workspace Module

</td><td>

Workforce Optimization for Customer Service module that displays the filter configuration.

</td></tr><tr><td>

Active

</td><td>

Enables the filter configuration in Manager Workspace.

</td></tr><tr><td>

Macroponent

</td><td>

Metadata defined seismic component.

</td></tr></tbody>
</table>4.  Click **Submit**.


**Parent Topic:**[Configuring Workforce Optimization for Customer Service](../concept/setup-configurable-wfo-cs.md)

