---
title: Define an EVAM configuration bundle
description: Create a view configuration to combine conditions, database fields, and declarative actions with an associated view template.
locale: en-US
release: xanadu
product: Entity View Action Mapper \(EVAM\)
classification: entity-view-action-mapper-evam
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [View configurations, view templates, and configuration bundles, Entity View Action Mapper, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Define an EVAM configuration bundle

Create a view configuration to combine conditions, database fields, and declarative actions with an associated view template.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Entity View Action Mapper \(EVAM\)** &gt; **View Definitions** &gt; **View Configurations**, and then click **New**.

2.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the EVAM view configuration.|
    |Active|Option to activate the EVAM view configuration.|
    |Required Roles|Roles to define who can view the EVAM view configuration|
    |View Template|Template to associate with the EVAM view configuration.|
    |Application|Application scope of the EVAM view configuration.|
    |Order|Priority that the EVAM view configuration takes over other view configurations. To give higher priority to a view configuration, enter a lower number.|
    |Table|Table to associate with the EVAM view configuration.|
    |Condition|Conditions for when to use the EVAM view configuration. Click **Add Filter Condition** to select which conditions should be met.|
    |Table Fields|Table fields to display on the EVAM view configuration. You can choose from available table fields and move them to **Selected**. You can also order the order they are shown.|
    |Custom Fields|A custom field to display on the EVAM view configuration. You must supply a comma-separated list of table fields are required for the template.|


