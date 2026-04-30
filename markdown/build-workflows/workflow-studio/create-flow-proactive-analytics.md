---
title: Create a flow with a Proactive Analytics trigger
description: Use Performance Analytics indicators to start a flow. Define the flow start conditions as a set of Proactive Analytics KPI scores and KPI threshold values.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Create a flow, Building flows, Use, Workflow Studio, Build workflows]
---

# Create a flow with a Proactive Analytics trigger

Use Performance Analytics indicators to start a flow. Define the flow start conditions as a set of Proactive Analytics KPI scores and KPI threshold values.

## Before you begin

**Important:** This flow supports Performance Analytics indicators inside Platform Analytics. The flow requires a subscription to Performance Analytics. Furthermore, you should have a working Performance Analytics implementation. For more information, see [Performance Analytics \(Indicator data sources\)](https://www.servicenow.com/docs/access?context=pa-overview&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US).

To create the flow, you should be familiar with Performance Analytics artifacts such as indicators and their associated targets and thresholds. You should also be familiar with your organization's Performance Analytics implementation. If you are not an expert in Performance Analytics, consider contacting such an expert from inside your organization. This expert can identify your organization's use cases for Proactive analytics triggers, which you can then implement. Even if you are only testing the flow, this expert can identify an appropriate indicator to test it on.

-   Activate your Platform Analytics subscription. See [Activating your Performance Analytics subscription](https://www.servicenow.com/docs/access?context=c_PremiumPerformanceAnalytics&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US).
-   Select the relevant Performance Analytics indicators \(KPIs\) and KPI Signals.
-   Run the **Proactive Analytics Trigger Definition Activation Job** from Schedule \[sys\_trigger\].

Role required: admin or flow\_designer

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  From the Workflow Studio home page, select **New** &gt; **Flow**.

3.  Define the flow properties.

    For more information, see [Create a flow in Workflow Studio](create-flow.md).

4.  In the Trigger section, add a trigger and select **Proactive Analytics**.

5.  For **Proactive analytics trigger**, select a trigger type.

    |Proactive Analytics trigger type|Description|
    |--------------------------------|-----------|
    |Predictive target missed|Start the flow when a KPI target is likely to be missed.|
    |Predictive threshold breached|Start the flow when a KPI threshold is likely to be breached.|
    |Signal generated|Start the flow when a KPI indicator generates a signal.|
    |Target missed|Start the flow when a KPI target is missed.|
    |Threshold all time|Start the flow when a KPI threshold is breached by an all-time high or low value.|
    |Threshold breached|Start the flow when a KPI threshold is breached.|

    **Note:** For more information about Proactive Analytics options, see [Proactive analytics insights on dashboards](https://www.servicenow.com/docs/access?context=proactive-analytics&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US).

6.  In **Condition**, select the KPI indicator, target, or threshold values needed to start the flow.

    The list of Conditions varies by Proactive Analytics trigger type. You can use the condition builder to add or remove conditions as needed.

    For example, start a flow when the Incidents opened since last 24 hours indicator generates a Short Run signal.

    ![Condition builder to start a flow when the Incidents opened since last 24 hours KPI generates a Short Run signal](../images/trigger-proactive-analytics-example.png)

7.  Add actions, subflows, and flow logic to the flow.

    For example, send a notification or create a task.

8.  Test the flow.

    For more information about testing a flow, see [Test a flow](flow-test.md).


**Parent Topic:**[Create a flow in Workflow Studio](create-flow.md)

**Related topics**  


[Performance Analytics indicators](https://www.servicenow.com/docs/access?context=c_Indicators&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)

[KPI Signals](https://www.servicenow.com/docs/access?context=process-behavior-charts-for-kpis&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)

[Performance Analytics targets and thresholds](https://www.servicenow.com/docs/access?context=pa-targets-thresholds&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)

