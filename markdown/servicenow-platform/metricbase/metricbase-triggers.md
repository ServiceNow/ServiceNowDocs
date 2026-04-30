---
title: Triggering flows using MetricBase data
description: Time-series data that is stored in the MetricBase database can trigger Workflow Studio flows. These triggers can log incidents, send emails, and create other alerts.
locale: en-US
release: yokohama
product: MetricBase
classification: metricbase
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [MetricBase, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Triggering flows using MetricBase data

Time-series data that is stored in the MetricBase database can trigger Workflow Studio flows. These triggers can log incidents, send emails, and create other alerts.

## Overview of implementing triggers

A trigger definition is a set of conditions that automatically executes a Workflow Studio flow. When you create a trigger definition in MetricBase and associate it with a flow, the trigger definition transfers from your instance to the MetricBase server. After you activate the trigger and flow, MetricBase monitors time-series data in the MetricBase database. When time-series data matches the initial triggering condition, and then transitions from one condition to the next, a transition trigger is generated and added to the queue. The instance polls the queue, processes the transition trigger, and then executes the Workflow Studio flow.

For more information about time-series policies, see [Create a time-series definition in MetricBase](../task/set-up-data-monitoring.md).

![Trigger workflow](../image/mb-glide-relationship.png "Trigger workflow")

1.  Define one or more triggers on an instance.
    -   **[Create a MetricBase band trigger](../task/create-metricbase-band-trigger.md)**

        Triggers when a metric value falls within a range of values.

    -   **[Create a MetricBase linear predictor trigger](../task/create-mb-linear-predictor-trigger.md)**

        Triggers when a series of values trend toward and are expected to reach a specified value.

    -   **[Create a MetricBase gap trigger](../task/create-metricbase-gap-trigger.md)**

        Triggers when values are not received for a specified period.

    -   **[Create a MetricBase model trigger](../task/create-metricbase-model-trigger.md)**

        Triggers when a trained model detects anomalous behavior.

2.  [Execute triggers conditionally](../task/create-action-condition.md)

    Create a trigger condition to add additional requirements for a trigger to execute a flow. For example, data often fluctuates over time. Small fluctuations can cause unwanted, duplicate triggering events. A Condition Script can prevent that erroneous duplication.

3.  [Assign a trigger to a flow](../task/assign-trigger-to-workflow.md)

    Associate the trigger with the flow it executes using Workflow Studio.

4.  Test the trigger and workflow.
5.  Activate the trigger.

## Deleting triggers

If a trigger is associated with a flow, you can't delete it in MetricBase. To delete a trigger, you must first delete the flow in Workflow Studio and then you can delete the trigger in MetricBase.

## Legacy triggers

Legacy triggers are deprecated. You can't create legacy triggers; you can only carry forward legacy triggers that exist.

