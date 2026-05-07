---
title: Analyze knowledge gaps from a demand insights dashboard and create knowledge gap feedback tasks
description: Use the demand insights dashboard for your tasks to analyze candidate knowledge gaps and create knowledge gap feedback tasks.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuration tasks for knowledge demand insights, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Analyze knowledge gaps from a demand insights dashboard and create knowledge gap feedback tasks

Use the demand insights dashboard for your tasks to analyze candidate knowledge gaps and create knowledge gap feedback tasks.

## Before you begin

You must have read access to the tasks that you want to analyze and the sn\_km\_ml.knowledge\_curation\_user role.

## About this task

A demand insights dashboard displays tasks as topics for which your knowledge bases do not have adequate knowledge coverage. You can create and assign knowledge gap feedback tasks for a topic so your knowledge bases can better be used to solve and deflect any issues described in a task. Tasks represent customer service cases, incidents, problems, and so on.

## Procedure

1.  Navigate to **Knowledge Demand Insights** and select the demand insights dashboard for your tasks, or navigate to **All** &gt; **Self-Service** &gt; **Dashboards**.

    -   For customer service cases, select **Demand Insights for Cases**.
    -   For incidents, select **Demand Insights for Incidents**.
    -   For HR cases, select **Demand Insights for HR cases**.
    **Note:** For tasks other than customer service cases, incidents, and HR cases, you can create another dashboard or update an existing dashboard. For more information, see [Create and use dashboards](https://www.servicenow.com/docs/access?context=create-and-edit-dashboards&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

2.  To view similar tasks grouped together, click a bar in the Pareto chart.

    Each bar represents a collection of similar tasks grouped together because they are likely to be on the same topic. The bars covering the largest number of tasks start from the left in a descending order. The blue line indicates how many bars you must analyze to cover 80% of all tasks that don't have good knowledge coverage. For more information, see [Pareto chart for Knowledge Demand Insights](../concept/pareto-report-demand-insights.md).

3.  To generate a representative sample to see a smaller list, in the Knowledge Curation Tasks list, click **Generate Representative Sample**.

    If the Knowledge Curation Tasks list is large, you can generate a representative sample subset of a Knowledge Curation Tasks list. This smaller list aims to accurately reflect the characteristics of the tasks included in the main list.

4.  Analyze the sample to create a knowledge gap feedback task or ignore the tasks within a collection.

<table id="choicetable_vcr_p5r_hlb"><thead><tr><th align="left" id="d296381e130">

Action

</th><th align="left" id="d296381e133">

Procedure

</th></tr></thead><tbody><tr><td id="d296381e139">

**Report a knowledge gap to create a feedback task**

</td><td>

1.  In the Knowledge Curation Tasks list, select tasks for which you want to create a knowledge gap.

**Note:** Any selected tasks already reported as knowledge gaps are automatically skipped.

2.  Click **Report Knowledge Gap**.
3.  In the **Description** field, describe the knowledge gap.

The **Description** field is automatically populated with frequently appearing words in the associated collection. You can overwrite the default description and enter a summary of your analysis so that knowledge authors have the necessary information to create an article from the feedback task.

4.  Click **Submit**.


</td></tr><tr><td id="d296381e179">

**Ignore a collection to avoid its tasks from being reported as knowledge gaps**

</td><td>

1.  In the Knowledge Curation Tasks list, click **Ignore Collection**.
2.  Click **OK** in the warning message that appears.


</td></tr></tbody>
</table>
## Result

If tasks within a collection are reported as knowledge gaps, a common feedback task for all the selected tasks is created and appears in the Knowledge Management application. You can use the assignment rules to assign a feedback task to an ownership group or author. In the Knowledge Curation Tasks list, the **Is knowledge gap created** column value for the selected tasks is set to **true**.

If you select an ignored collection from the demand insights dashboard, you can no longer report tasks within the collection as knowledge gaps.

**Parent Topic:**[Configuration tasks for knowledge demand insights](../concept/configuration-tasks-for-knowledge-demand-insights.md)

**Related topics**  


[Demand Insights for Cases dashboard](../concept/demand-insights-cases-dashboard.md)

[Demand Insights for Incidents dashboard](../concept/demand-insights-incidents-dashboard.md)

