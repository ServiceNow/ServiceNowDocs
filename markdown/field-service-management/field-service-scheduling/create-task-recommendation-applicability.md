---
title: Map applications to Intelligent Task Recommendation policies
description: Map applications to task recommendation policies. Provide access to these policies within those applications.
locale: en-US
release: zurich
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Set up Intelligent Task Recommendations, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Map applications to Intelligent Task Recommendation policies

Map applications to task recommendation policies. Provide access to these policies within those applications.

## Before you begin

Role required: admin, wm\_admin

## About this task

By default, Dispatcher Workspace and Mobile are mapped to a task recommendation policy.

## Procedure

1.  Navigate to **Field Service** &gt; **Task Recommendation Administration** &gt; **Task Recommendation Applicabilities**.

2.  Click **New**.

3.  On the form, fill the fields.

    |Field|Description|
    |-----|-----------|
    |Display Name|Display name of the recommendation application.|
    |Name|Name of the recommendation application.|
    |Table|Task table that is selected for the recommendation policy.|
    |Application module|Module of the application. This field is automatically set to **Field Service Management**.|
    |Active|Option to indicate whether the application is available for consideration when recommending work order tasks.|
    |Default task recommendation policy|The default task recommendation policy for this application.|
    |Application|Application that contains this record.|

4.  Click **Submit**.


**Related topics**  


[Assign work order tasks to agents using Intelligent Task Recommendation](../concept/manage-work-order-tasks-dw.md#)

[Assign tasks to yourself based on Intelligent Task Recommendation](recommend-task-fsm-mobile.md)

