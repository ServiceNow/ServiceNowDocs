---
title: Historical data generation for metrics
description: Historical data generation creates metric definition data, metric data, and metric data tasks for past periods. If the metric belongs to an active, published campaign, the system also creates campaign cycles for those periods.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/environmental-social-governance/historical-data-generation-for-metrics.html
release: zurich
topic_type: concept
last_updated: "2026-09-30"
reading_time_minutes: 3
keywords: [historical data, historical start date, create historical data]
breadcrumb: [Exploring GRC: Metrics, GRC: Metrics, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Historical data generation for metrics

Historical data generation creates metric definition data, metric data, and metric data tasks for past periods. If the metric belongs to an active, published campaign, the system also creates campaign cycles for those periods.

To generate records for past periods, you select the **Create historical data** option on a metric and enter a **Historical start date**. The historical start date must be earlier than today.

## How historical data generation works

Records are created for every period, at the metric's frequency, from the historical start date up to the most recent completed period. Current and future periods are skipped and continue to be generated on their regular schedule. Metric definition data is also created for each historical period.

Saving the metric doesn't generate historical records. They're generated the next time metric data is created for the metric, in one of these ways:

-   The scheduled job runs when the metric's **Next run date** is reached.
-   You select **Execute** on the metric definition.

    **Note:** Selecting **Execute** on an individual metric doesn’t generate historical records. It creates or updates data for the current period only.


For example, if the historical start date for a monthly metric is 1 January and its next scheduled run is in mid-April, historical records are created for January, February, and March only. April is still in progress, so its records are generated on the regular schedule.

**Note:** After historical records are generated, the **Create historical data** option is cleared automatically, so that future runs don't generate them again.

The historical records created for each period depend on the metric type:

-   Manual metric: Metric data and a metric data task.
-   Automated metric that creates tasks: Metric data and a metric data task. An automated metric creates tasks when task creation is enabled on its metric definition or when the metric belongs to a campaign.
-   Automated metric that doesn't create tasks: Metric data only, which is completed with the calculated value.

The new historical records start in the following states.

|Record|Manual metric|Automated metric|
|------|-------------|----------------|
|Metric data|Pending|Pending, or Completed when no task is created|
|Metric data task|New|In Progress|
|Campaign cycle \(campaign metrics only\)|Data collection|Data collection|

If historical records already exist for a period, they aren't duplicated. For example, if the metric already has a January task from a previous run, historical records are created only for February and March.

## Historical data for a metric in a campaign

Historical data generation creates one metric data task for each past period. If the metric belongs to an active, published campaign, each task is added to the campaign's cycle for the same period.

-   When a campaign cycle already exists, the historical metric data task is added to it. For example, if the campaign already has a March cycle, the metric's March task is added to that cycle. A second March cycle isn't created.
-   When a campaign cycle doesn't exist for a period, one is created, even if the period is before the campaign's first run date. For example, if the campaign's first run date is in March, then January and February cycles are created for the metric's January and February tasks.

If the metric already has a metric data task for a past period, that period is skipped, so no campaign cycle is created for it. For example, if a metric already has a March task, the historical run skips March for this metric. No task is created, and no cycle is created or linked.

## Historical data in campaign cycles that are already closed

A historical metric data task might be added to a campaign cycle that's already in the Approval or Closed state. In such cases, the outcome depends on whether bulk actions are enabled by the bulk submission system property.

**Note:** To change this property, navigate to **All** &gt; **Operational Sustainability Management** &gt; **Properties**. Changing the property doesn't affect campaign cycles that were already processed or historical data that was already created.

-   **When bulk submission is enabled**

    All metric data tasks in a cycle must be in the same state, so the cycle reopens to the Data collection state. Other metric data tasks in the cycle that are in the Awaiting Approval, Closed, or Estimated state move to In Progress, and their metric data moves to Pending.

-   **When bulk submission is disabled**

    The cycle keeps its current state. Other metric data tasks in the cycle also keep their current state.


