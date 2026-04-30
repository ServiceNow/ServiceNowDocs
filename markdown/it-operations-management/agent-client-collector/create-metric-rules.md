---
title: Create metric rules
description: Create a metric rule to determine the metric, the threshold values and ranges, and the severity level of generated events. You can add a filter that determines the Configuration Items \(CI\) types or resources for which you receive alerts. For example, you can configure a filter to receive alerts only for Windows servers.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Activating Metric Intelligence, Metric Intelligence, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# Create metric rules

Create a metric rule to determine the metric, the threshold values and ranges, and the severity level of generated events. You can add a filter that determines the Configuration Items \(CI\) types or resources for which you receive alerts. For example, you can configure a filter to receive alerts only for Windows servers.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

When a metric crosses or falls within the range of a configured threshold, the system creates a single event, which is eventually processed into an IT alert. The severity of the event \(and alert\) is determined by a defined threshold, and the event is bound to a CI.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Metrics** &gt; **Metric Rules**.

2.  Select **New Metric Rule**.

    The **CI selection** page opens.

3.  Select the CI class on which to run the rule in the **CI Class** field.

    Only CIs containing metrics are available for selection.

4.  Apply a filter within the selected CI class.

    For example, if you selected a CI class of **Linux Server**, you can apply a filter to indicate that the rule applies only to those servers with a host name that starts with a specified string.

5.  Select **Next**.

    The **Alert criteria** page opens.

6.  Select the metric and criteria to create an alert.

    1.  Select the alert severity that you want to configure in the **Alert severity** field.

        Choose from the following:

        -   Critical
        -   Major
        -   Minor
        -   Warning
    2.  Select the metric for the alert severity to apply to in the **Metric** field.

    3.  Select the comparison operator \(equals, is greater than, is greater than or equals, and so forth\) in the **Comparison operator** field.

    4.  Enter a value in the **Value** field.

    For example, you can configure criteria to indicate that when the metric **node\_rx\_packets** is greater than 10, a Critical alert is generated.

    To define additional alert severities, select **Add another alert severity** and repeat this step.

7.  Select when to generate the alert in the **Alert when** section.

    Choose from the following:

    -   **All sampled values must breach the criteria in the following time period**.

        Select the time period, in minutes.

    -   **Average of sampled values in the following time period must breach the criteria**.

        Select the time period, in minutes.

    -   **Any time the sampled values breach the criteria**.
8.  Select **Next**.

    The **Name and activation** page opens.

9.  Verify the name and details of the metric rule.

    To activate the rule, ensure that the **Active** toggle switch ![Active toggle switch.](../image/active-toggle-switch.png) is activated.

10. Select **Finish**.


**Parent Topic:**[Activating Metric Intelligence](../concept/activating-metric-intelligence.md)

