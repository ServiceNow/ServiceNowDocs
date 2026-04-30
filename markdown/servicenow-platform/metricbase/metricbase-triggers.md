---
title: Triggering flows using MetricBase data
description: Time-series data that is stored in the MetricBase database can trigger Workflow Studio flows. These triggers can log incidents, send emails, and create other alerts.
locale: en-US
release: xanadu
product: MetricBase
classification: metricbase
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [MetricBase, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Triggering flows using MetricBase data

Time-series data that is stored in the MetricBase database can trigger Workflow Studio flows. These triggers can log incidents, send emails, and create other alerts.

A trigger definition is a set of conditions that automatically executes a Workflow Studio flow. When you create a trigger definition in MetricBase and associate it with a flow, the trigger definition transfers from your instance to the MetricBase server. After you activate the trigger and flow, MetricBase monitors time-series data in the MetricBase database. When time-series data matches the initial triggering condition, and then transitions from one condition to the next, a transition trigger is generated and added to the queue. The instance polls the queue, processes the transition trigger, and then executes the Workflow Studio flow.

![Trigger workflow](../image/mb-glide-relationship.png "Trigger workflow")

For more information about time-series policies, see [Create a time-series definition in MetricBase](../task/set-up-data-monitoring.md).

## High-level overview of implementing triggers

1.  Define one or more triggers on an instance.
    -   **Band trigger**

        Triggers when a metric value falls within a range of values.

    -   **Linear predictor trigger**

        Triggers when a series of values trend toward and are expected to reach a specified value.

    -   **Gap trigger**

        Triggers when values are not received for a specified period.

    -   **Model trigger**

        Triggers when a trained model detects anomalous behavior.

2.  Create a trigger condition to add additional requirements for a trigger to execute a flow.

    For example, data often fluctuates over time. Small fluctuations can cause unwanted, duplicate triggering events. A Condition Script can prevent that erroneous duplication.

3.  Associate the trigger with the flow it executes using Workflow Studio.
4.  Test the trigger and workflow.
5.  Activate the trigger.

## Deleting triggers

If a trigger is associated with a flow, you can't delete it in MetricBase. To delete a trigger, you must first delete the flow in Workflow Studio and then you can delete the trigger in MetricBase.

## Legacy triggers

Legacy triggers are deprecated. You can't create legacy triggers; you can only carry forward legacy triggers that exist.

