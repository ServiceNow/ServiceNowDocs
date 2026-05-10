---
title: Define an EVAM view configuration
description: Create a view configuration to combine conditions, database fields, and declarative actions with an associated view template.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Customize dynamic related records, Playbook pages, Playbooks in Customer Service Management, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Define an EVAM view configuration

Create a view configuration to combine conditions, database fields, and declarative actions with an associated view template.

## Before you begin

Role required: admin or evam\_admin

## About this task

Entity View Action Mapper \(EVAM\) is an application that standardizes how different data sources display in cards and lists.

A view configuration combines conditions, database fields, and declarative actions with an associated view template. For more information, see [View configurations, view templates, and configuration bundles for EVAM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/entity-view-action-mapper-evam/use-configuration-bundle.md).

## Procedure

1.  Navigate to **All** &gt; **Entity View Action Mapper \(EVAM\)** &gt; **EVAM Definitions** &gt; **Configuration Bundles**.

2.  Select **dynamic\_related\_records\_bundle** and then select **New**.

3.  Fill in the fields on the EVAM view configuration form.

<table id="table_fhj_dsy_2nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the EVAM view configuration.

</td></tr><tr><td>

Active

</td><td>

Option to activate the EVAM view configuration.

</td></tr><tr><td>

View Template

</td><td>

Template to associate with the EVAM view configuration. You can create a template or use an existing template.

</td></tr><tr><td>

Application

</td><td>

Application scope of the EVAM view configuration.

</td></tr><tr><td>

Order

</td><td>

Priority that the EVAM view configuration takes over other view configurations. To give higher priority to a view configuration, enter a lower number.

</td></tr><tr><td>

Table

</td><td>

Table to associate with the EVAM view configuration.

</td></tr><tr><td>

Condition

</td><td>

Conditions for when to use the EVAM view configuration.

</td></tr><tr><td>

Table Fields

</td><td>

Table fields to display on the EVAM view configuration. For example:`name,supplier,description,product_category`

</td></tr><tr><td>

Custom Fields

</td><td>

Custom fields to display on the EVAM view configuration. This is a comma-separated list of non-table fields that are required for the template. For example:`price,image_url,delivery_label,delivery_date,product_url`

</td></tr></tbody>
</table>4.  Select **Save**.

5.  Create an M2M action assignment or select **Link Existing** and then select the Declarative Action **navigation**.

    For more details, see, [View configurations, view templates, and configuration bundles for EVAM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/entity-view-action-mapper-evam/use-configuration-bundle.md).


**Related topics**  


[Configure dynamic related records](../concept/dynamic-related-records-configure.md)

[Configure related record definitions](configure-related-record-definitions.md)

