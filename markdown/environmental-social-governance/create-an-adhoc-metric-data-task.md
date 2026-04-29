---
title: Create ad hoc metric data tasks
description: Handle off-cycle requests for up-to-date information on existing metric definitions and metrics by creating ad hoc metric data tasks. These tasks address off-cycle requests and provide the latest information.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using GRC: Metrics to provide data, GRC: Metrics, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Create ad hoc metric data tasks

Handle off-cycle requests for up-to-date information on existing metric definitions and metrics by creating ad hoc metric data tasks. These tasks address off-cycle requests and provide the latest information.

## Before you begin

Role required: sn\_grc\_metric.manager

## About this task

When you create an ad hoc task, it is automatically assigned to the data owner specified in the metric definition form. It is important to note that for manual metric definitions these ad hoc tasks:

-   do not contribute to the aggregated metric definition data.
-   are not considered for entity hierarchy rollup.
-   are not evaluated for threshold rating, Variance\(%\)

However, for calculated metric definitions that have the **Calculation level** field set to **Entity**, the ad hoc tasks data contribute to the metric score.

## Procedure

1.  Navigate to **All** &gt; **Operational Sustainability Management** &gt; **Operational Sustainability Workspace** &gt; **Lists** &gt; **Metrics** &gt; **Manual metric definitions**.

2.  Select and open the required metric definition.

3.  Open the metric for which you want to create ad hoc tasks.

4.  Select **Create ad hoc task**.

5.  In the Ad hoc metric data task dialog box, provide the start date, end date, and due date of the task.

6.  Select **Submit**.


## What to do next

For information about features that are not supported for ad hoc metric data tasks, see [Ad hoc metric data task limitations](../reference/ad-hoc-metric-data-task-limitations.md).

-   **[Ad hoc metric data task limitations](../reference/ad-hoc-metric-data-task-limitations.md)**  
Ad hoc metric data tasks don't support certain features that are available for scheduled metric data tasks.

**Parent Topic:**[Using GRC: Metrics to provide data](../concept/using-grc-metrics.md)

