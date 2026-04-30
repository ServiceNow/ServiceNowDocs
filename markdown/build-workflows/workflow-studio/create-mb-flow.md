---
title: Create a flow with a MetricBase trigger
description: Start a flow when a MetricBase trigger is met. MetricBase triggers track time series data and can monitor when a threshold is reached, when a trend is detected, or when a system stops reporting data.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create a flow, Building flows, Use, Workflow Studio, Build workflows]
---

# Create a flow with a MetricBase trigger

Start a flow when a MetricBase trigger is met. MetricBase triggers track time series data and can monitor when a threshold is reached, when a trend is detected, or when a system stops reporting data.

## Before you begin

Role required: flow\_designer or admin

MetricBase triggers are not available on the base system. The MetricBase application requires a separate subscription and must be activated by ServiceNow personnel.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Click **+ New** &gt; **New Flow**.

3.  Define the flow properties.

    For more information, see [Create a flow in Workflow Studio](create-flow.md).

4.  In the Trigger section, add a trigger and select **MetricBase**.

5.  Complete the trigger fields.

    |Field|Description|
    |-----|-----------|
    |MetricBase Trigger|Select or create a MetricBase trigger record to start the flow. For types of MetricBase triggers, see [MetricBase triggers](https://www.servicenow.com/docs/access?context=metricbase-triggers&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).|
    |Table|Read-only table that contains the metric.|
    |Condition|Click **Add filters** to set field-based conditions that determine when the flow runs.|
    |Condition Script|Define a script in the Additional MetricBase Trigger Filtering and Moderation table to prevent duplicate metric events from re-triggering a flow. For example, if a metric hovers at a defined trigger threshold, create a script that defines whether to run the flow once when the metric is met, or every time the triggering threshold is exceeded.|

6.  Add actions, subflows, and flow logic to the flow.

7.  Test the flow.

8.  Once the flow is behaving as desired, activate the flow.

    For more information, see [Test a flow](flow-test.md) and [Activate a flow](flow-activate.md).


## Result

The MetricBase application monitors time series data on the ServiceNow AI Platform. When the selected trigger is met, the flow runs.

**Parent Topic:**[Create a flow in Workflow Studio](create-flow.md)

