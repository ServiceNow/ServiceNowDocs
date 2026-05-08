---
title: Configure the mapping of solution definitions with task tables
description: Configure the combination of the task table and similarity and clustering solution definitions that are processed in a scheduled job for a task type. You can create another demand insights configuration or modify an existing configuration to define a scheduled job for demand insights.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuration tasks for knowledge demand insights, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure the mapping of solution definitions with task tables

Configure the combination of the task table and similarity and clustering solution definitions that are processed in a scheduled job for a task type. You can create another demand insights configuration or modify an existing configuration to define a scheduled job for demand insights.

## Before you begin

This task describes the process for configuring a scheduled job.

Instead of doing the configuration through this procedure, consider using a guided setup. Navigate to **Knowledge** &gt; **Administration** &gt; **Guided Setup**, click **Get Started**, and then scroll to the Knowledge Demand Insights section.

Ensure that you have configured a similarity type and clustering type solution definitions for a task type. For more information, see [Configure solution definitions to find gaps in a knowledge base](configure-km-solution-defintions.md).

Role required: admin

## About this task

A scheduled job for each task type runs business rules and then executes the similarity and clustering solution definitions. In the Demand Insights Configuration module, you configure the combination of the task table and similarity and clustering solution definitions that are processed in a scheduled job for a task type. This configuration is optional for customer service cases and incidents.

**Note:** For task types other than customer service cases and incidents, a user with the admin role must also perform the following tasks:

-   Assign the sn\_km\_ml.knowledge\_curation\_user role and the appropriate roles for the task type to the users performing the knowledge gap analysis. To assign roles, perform the Assign knowledge curator roles guided setup task, which are available in the Knowledge Demand Insights section of the Knowledge Management guided setup.
-   Create a demand insights dashboard for the task type. To create a dashboard, see Create or configure a responsive dashboard.

## Procedure

1.  Navigate to **All** &gt; **Knowledge Demand Insights** &gt; **Demand Insights Configuration**.

2.  Configure the combination of the task table and similarity and clustering solution definitions that are processed in a scheduled job.

    -   For customer service cases, select **sn\_customerservice\_case**.
    -   For incidents, select **incident**.
    -   For HR cases, select **sn\_hr\_core\_case**.
    -   For tasks other than customer service cases, incidents, and HR cases, click **New** to create another combination.
3.  On the KB curation configuration form, verify the default field values for customer service cases or incidents or fill in the values for a custom configuration.

    |Field|Description|
    |-----|-----------|
    |Curation table|Name of the table you want the data to pull information from. For example, for customer service cases, select Case \[sn\_customerservice\_case\] and for incidents select Incident \[incident\].|
    |Fields|Fields in the curation table that include the ID of knowledge articles, for example, the knowledge article ID KB07276660 in the field resolution notes,|
    |Query condition|Conditions for filtering the number of tasks from the curation table. You can create conditions using the condition builder \(see Condition builder\).|
    |Similarity solution definition|Similarity solution definition for your task type. For example, for customer service cases, select **Demand Insights: Similar Cases and Knowledge**.|
    |Clustering solution definition|Clustering solution definition for your task type. For example, for customer service cases, select **Demand Insights: Case Clusters Need Knowledge**.|

4.  Click **Update** for incidents or customer service cases or **Submit** to save a custom configuration.


## What to do next

Set the frequency of the scheduled job for your task. For more information, see [Set the frequency of knowledge gap analysis](run-gap-analysis-periodically-demand-insights.md).

**Parent Topic:**[Configuration tasks for knowledge demand insights](../concept/configuration-tasks-for-knowledge-demand-insights.md)

**Related topics**  


[Configure solution definitions to find gaps in a knowledge base](configure-km-solution-defintions.md)

