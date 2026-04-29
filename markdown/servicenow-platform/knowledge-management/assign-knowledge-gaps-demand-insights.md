---
title: Assign knowledge gap feedback tasks to content authors
description: Create assignment rules to assign knowledge gap feedback tasks to authors or groups of content creators.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuration tasks for knowledge demand insights, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Assign knowledge gap feedback tasks to content authors

Create assignment rules to assign knowledge gap feedback tasks to authors or groups of content creators.

## Before you begin

Role required: admin or assignment\_rule\_admin

## About this task

Knowledge gap feedback tasks created through the Knowledge Demand Insights feature create feedback tasks of type **Knowledge gap**.

## Procedure

1.  Navigate to **All** &gt; **Knowledge Demand Insights** &gt; **Knowledge Gap Assignment**.

2.  In the Assignment Rules list, click **New**.

3.  On the Assignment rule form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Descriptive name for the assignment rule.|
    |Active|Option to activate the assignment rule. Only active assignment rules take effect.|
    |Applies to tab|
    |Table|Table to store the feedback tasks on knowledge articles. This field is automatically set to **Knowledge Feedback Task \[kb\_feedback\_task\]**.|
    |Conditions|Conditions for assigning feedback tasks of the Knowledge gap type. This field is automatically set to **\[Feedback Task Type\] \[is\] \[Knowledge gap\]**. You can add more conditions as appropriate.|
    |Assign to tab|
    |User|User assigned the feedback task type of knowledge gap.|
    |Group|Ownership group assigned the feedback task type of knowledge gap.|
    |Script tab|
    |Script|Script you can use to specify more complex conditions for assignment rules using dynamic variables and loops.|

4.  Click **Submit**.


**Parent Topic:**[Configuration tasks for knowledge demand insights](../concept/configuration-tasks-for-knowledge-demand-insights.md)

**Related topics**  


[Create an assignment rule](https://www.servicenow.com/docs/access?context=t_AssignmentModuleRule&version=australia&pubname=australia-platform-administration&ft:locale=en-US)

[Analyze knowledge gaps from a demand insights dashboard and create knowledge gap feedback tasks](analyze-knowledge-gaps-demand-insights.md)

