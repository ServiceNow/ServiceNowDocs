---
title: Create an outage from a task
description: Create an outage from a task record to understand the down time of a configuration item.
locale: en-US
release: xanadu
product: Task Outage
classification: task-outage
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Task Outage, IT Service Management]
---

# Create an outage from a task

Create an outage from a task record to understand the down time of a configuration item.

## Before you begin

Role required: itil or admin

## About this task

The **Create Outage** UI action is added for the Task \[task\] table. When the Task-Outage Relationship plugin \(com.snc.task\_outage\) is activated, the Outages related list is added to the related list of the task forms such as Incident, Problem, or Change. If you have the admin role, you can assign multiple tasks to an outage by configuring the Tasks related list to appear on the Outages form.

## Procedure

1.  Open the task record.

2.  Right-click the header form and select **Create Outage**.

3.  On the form, fill in the fields.

    |Field|Entry|
    |-----|-----|
    |Number|Unique number that identifies the outage.|
    |Configuration Item|Look up icon ![Look up icon](../../itsm-workspace/image/look-up-icon.png) to select configuration item from the list.|
    |Type|Type of the outage.|
    |Begin|The date and time when the outage starts. You can click the **Begin Outage Now** related link to populate the field with the current date and time.|
    |End|The date and time when the outage ends. When the outage ends, open the record and enter the date and time manually. You can also click the **End Outage Now** related link to populate the field with the current date and time.|
    |Duration|Duration of the outage in days and hours.|
    |Task number|The parent task record number from which you have created the outage.|
    |Short description|A brief description of the outage.|

4.  Click **Submit**.


**Parent Topic:**[Task Outage](../concept/task-outage.md)

