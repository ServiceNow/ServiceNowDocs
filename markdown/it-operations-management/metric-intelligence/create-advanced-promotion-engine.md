---
title: Create a definition for the Advanced Promotion Engine
description: Create a definition for the Advanced Promotion Engine so that you can define the conditions for promoting the anomaly alerts to IT alerts. By promoting the alerts that meet the conditions, only the most relevant alerts move to the table.
locale: en-US
release: zurich
product: Metric Intelligence
classification: metric-intelligence
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Optimizing Metric Intelligence, Metric Intelligence, IT Operations Management]
---

# Create a definition for the Advanced Promotion Engine

Create a definition for the Advanced Promotion Engine so that you can define the conditions for promoting the anomaly alerts to IT alerts. By promoting the alerts that meet the conditions, only the most relevant alerts move to the table.

## About this task

IT Alerts appear in the Express List and are addressed by an operator.

Only metrics that are associated with a metric configuration rule that has **Anomaly score level = Anomaly alerts** are considered for promotion to IT alerts. For details on metric configuration rules, see [Metric Configuration Rules](../concept/metric-configuration-rule.md).

## Before you begin

Ensure that the Metric Intelligence plugin \(com.snc.sa.metric\) is installed.

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Advanced Promotion Engine** &gt; **Advanced Promotion Definitions**.

2.  Select **New**.

3.  In the **Name** field, enter a descriptive name for the definition.

4.  In the **Order** field, set the execution order for the definition.

    The definitions with a lower order are executed first.

5.  Activate the definition by selecting the **Active** check box.

6.  On the **CIs** tab, fill in the fields for the CI aIerts that you want to consider for promotion.

<table id="table_fb2_dzd_jwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CI class

</td><td>

CI class alerts to be promoted to the All Alerts table.

</td></tr><tr><td>

Filter

</td><td>

Filter to restrict which CIs that the definition applies to.Select **New Criteria** to configure the conditions that the definition applies to. You can add more conditions by selecting either **OR** or **AND**.

</td></tr><tr><td>

Skip CIs that were created less than this number of days ago

</td><td>

Number of days in the past that any CI created during that time is ignored. For example, a value of 7 indicates that any CIs created less than 7 days ago are not considered for promotion to the All Alerts table.

</td></tr></tbody>
</table>7.  On the **Severity** tab, enter the minimum severity of alerts to be considered for promotion.

    Alerts with the indicated severity level and higher levels are considered for promotion.

8.  On the **Number of Alerts** tab, in the **Number of alerts on CI** field, enter the minimum number of a CI's alerts with an identical severity level \(or higher\) to be considered for promotion.

    For example, a value of 3 indicates that at least three alerts with the indicated severity \(or higher\) must exist on a CI for the alert to be considered for promotion.

9.  On the **Time Window** tab:

    -   In the **Consider alerts updated at least this number of minutes ago** field, enter the minimum number of minutes old for an alert to be considered for promotion.

        For example, if the value of the field is 5, only alerts that are updated at least five minutes ago are considered for promotion.

    -   In the blue box, select the number of minutes link to modify the amount of minutes during which alerts are to be considered for promotion.

        The **Properties** page opens and you modify the value in the **The width of the time...** field.

        Default = 30.

    For example:

    -   The current time is 10:05.
    -   In the **The width of the time...** field, you entered a value of 30.
    -   In the **Consider alerts updated at least this number of minutes ago** field, you entered 5.
    Alerts that occur between 9:30-10:00 are considered for promotion.


## What to do next

Ensure that the a metric configuration rule exists which includes metrics you want to be promoted to an IT alert, and that the anomaly score level of the rule is **Anomaly alerts**. For details on configuring a metric configuration rule, see [Create a configuration settings rule](../../event-management/task/create-config-overriding-rule.md).

**Parent Topic:**[Optimizing Metric Intelligence](../../metric-intelligence/concept/optimizing-metric-intelligence.md)

