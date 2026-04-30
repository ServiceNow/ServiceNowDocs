---
title: Set the frequency of knowledge gap analysis
description: Set the frequency of the scheduled job for your task to automatically run knowledge gap analysis.
locale: en-US
release: xanadu
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuration tasks for knowledge demand insights, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Set the frequency of knowledge gap analysis

Set the frequency of the scheduled job for your task to automatically run knowledge gap analysis.

## Before you begin

This task describes the process for setting the frequency of knowledge gap analysis.

Instead of doing the configuration through this procedure, consider using a guided setup. Navigate to **Knowledge** &gt; **Administration** &gt; **Guided Setup**, click **Get Started**, and then scroll to the Knowledge Demand Insights section.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Knowledge Demand Insights** &gt; **Scheduled Jobs**.

2.  In the Scheduled Jobs list, select the scheduled job for your tasks in the **Name** column.

    -   For customer service cases, select **\[Knowledge Curation\]: Generate Case Clusters**.
    -   For incidents, select **\[Knowledge Curation\]: Generate Incident Clusters**.
    -   For HR cases, select **\[Knowledge Curation\]: Generate HR Case Clusters**.
    -   For tasks other than customer service cases, incidents, and HR cases, create another scheduled job. For more information, see [Create a scheduled job](https://www.servicenow.com/docs/access?context=t_CreateAScheduledJob&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).
3.  On the Scheduled Script Execution form, either accept the default value of running the analysis once a quarter \(every 90 days\) or change the frequency.

    **Note:** For best performance results, try not to perform knowledge gap analysis more frequently than once a month.

4.  Click **Update**.

    **Note:** If the application scope is not set to Knowledge Management - Machine Learning, a warning message appears and the **Update** button is not available. Click the word **here** at the end of the message to change the scope and click **Update**.

5.  To run the job immediately, click **Execute Now**.


## Result

The knowledge gap analysis is repeatedly run at the duration as configured in the scheduled job.

## What to do next

Create assignment rules to assign knowledge gap feedback tasks. For more information, see [Assign knowledge gap feedback tasks to content authors](assign-knowledge-gaps-demand-insights.md).

**Parent Topic:**[Configuration tasks for knowledge demand insights](../../../configuration-tasks-for-knowledge-demand-insights.md)

**Related topics**  


[Analyze knowledge gaps from a demand insights dashboard and create knowledge gap feedback tasks](analyze-knowledge-gaps-demand-insights.md)

