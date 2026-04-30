---
title: Create requester mapping
description: Create a requester mapping to extend the Zoom chat functionality to other tables.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Chat-specific configuration for Collaboration services for Zoom, Enhance employee experience by integrating ServiceNow with Zoom, Integrating and using ServiceNow with Zoom, ServiceNow for Zoom, Zoom integrations, Unified Employee Experience, Employee Service Management]
---

# Create requester mapping

Create a requester mapping to extend the Zoom chat functionality to other tables.

## Before you begin

Role required: admin

## About this task

A requester-mapping record defines which field is representing the requester of a ticket in any given table.

**Note:**

If there’s no requester mapping defined for a table, the interaction records aren’t created. An error log is created for the admin to notify that the requester mapping isn’t defined for a table.

## Procedure

1.  Navigate to **All** &gt; **Collaboration Services** &gt; **Requester Mapping**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_bxx_bjd_gvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Table to which the requester mapping should be applied.

</td></tr><tr><td>

Requester field

</td><td>

Field to select the requester for a record.

</td></tr><tr><td>

Inherit

</td><td>

Extends and applies the feature to the child tables.

</td></tr><tr><td>

Active

</td><td>

Option to activate the requester-mapping record.

</td></tr><tr><td>

Order

</td><td>

Order of the configuration.

 You can define multiple chat configuration for a single table. The system executes the query in the descending order.

</td></tr></tbody>
</table>4.  Select **Submit**.


**Parent Topic:**[Chat-specific configuration for Collaboration services for Zoom](../concept/additional-configuration-sn-cs-zoom.md)

