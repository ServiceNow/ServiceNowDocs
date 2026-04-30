---
title: Configure Knowledge Demand Insights
description: Configure the Knowledge Demand Insights feature to identify which topics are missing knowledge articles and creating actionable knowledge gaps for missing topics.
locale: en-US
release: zurich
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configuration tasks for knowledge demand insights, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure Knowledge Demand Insights

Configure the Knowledge Demand Insights feature to identify which topics are missing knowledge articles and creating actionable knowledge gaps for missing topics.

## Before you begin

Activate the Predictive Intelligence for Knowledge Management plugin \(com.snc.knowledge\_ml\). For more information, see [Predictive Intelligence for Knowledge Management](../concept/predictive-intelligence-for-km.md) and [Additional plugins for Knowledge Management](../reference/additional-plugins-km.md).

## About this task

To configure the Knowledge Demand Insights feature, use the Knowledge Management guided setup. The guided setup takes you through the entire setup and configuration process.

This task provides general steps to configure the Knowledge Demand Insights feature. For more information about the feature, see [Knowledge demand insights](../concept/knowledge-demand-insights.md).

## Procedure

1.  [Configure similarity and clustering solution definitions to enable comparing knowledge bases with a task type](configure-km-solution-defintions.md).

2.  [Configure the combination of the task table and similarity and clustering solution definitions that are processed in a scheduled job for a task type](select-tasks-knowledge-bases.md).

3.  [Configure scheduled jobs for each task](run-gap-analysis-periodically-demand-insights.md).

4.  [Configure assignment rules to automatically assign feedback tasks of type Knowledge gap](assign-knowledge-gaps-demand-insights.md).

    **Note:** If no assignment rules are configured, a knowledge admin or knowledge manager can later use the Feedback Management feature in the Knowledge module to manually assign a feedback task.


**Parent Topic:**[Configuration tasks for knowledge demand insights](../concept/configuration-tasks-for-knowledge-demand-insights.md)

**Related topics**  


[Analyze knowledge gaps from a demand insights dashboard and create knowledge gap feedback tasks](analyze-knowledge-gaps-demand-insights.md)

