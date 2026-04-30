---
title: Configure an activity definition
description: Report on steps that occur within your business process.
locale: en-US
release: xanadu
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Create a project using Classic view, Using Process Mining, Process Mining, Platform Analytics]
---

# Configure an activity definition

Report on steps that occur within your business process.

## Before you begin

Role required: sn\_process\_optimization\_analyst, sn\_process\_optimization\_power\_user, or sn\_process\_optimization\_admin

-   [Create a project or template using Project Builder](define-workflow-model.md)

**Note:** You can configure a maximum of 10 activity definitions for the parent table configuration and 5 activity definitions for any child table configuration. You cannot generate more than 5000 elements for any activity definition.

## About this task

Process Mining gathers audit log field data for activities you define. Configure at least one activity to extract for and display in your process map records that start, end, or pass through a specific activity.

**Note:** While configuring a project, you must first set up a main \(parent\) table configuration, define an activity definition, and set up a breakdown definition. If only one table is needed, you can generate a full project that you can periodically mine and schedule with the data. If multiple tables are required, you must create additional \(child\) tables, relate it to the main \(parent\) table, and define the activity definition. You may also configure breakdown definitions on child tables.

You can set up dot walking on activities that will flag any kind of change that you want to keep a track of.

Large organizations find it inefficient or non-compliant to change Configuration Items \(CIs\) and business services, especially when they're associated with legal and geographical entities. To address this, they perform data mining on dot-walked fields for insights without changing these critical attributes.

While adding activity definitions, you can add a reference field \(dot walked field\) to flag any such non-compliance. For example: Assigned\_to.Location. After the mining is complete, the graph will display the data flow across different locations making it easier for you to track any non-compliance.

You can also group multiple activities to track changes made to each of the activities. For this, you can add an activity definition of type "Compound" and select the fields. After the mining is complete, the graph will display that something has changed for these fields. This will simplify the graph. To know the details, you can further filter them.

## Procedure

1.  From the **Activity Definitions** tab of your table configuration record, select **New**.

2.  On the form, fill in the fields.

    For a description of the field values, see [Activity definition form](../reference/activity-def.md).

3.  Select **Submit**.


## What to do next

Configure a breakdown or generate a project.

**Parent Topic:**[Create a project using Classic view](create-proj.md)

