---
title: Set a threshold to suppress alert generation
description: The event threshold is the rate upon which Event Management generates an alert. Receiving multiple events for a device over a short interval may warrant creating an alert, as the condition may be serious. However, receiving events over a longer interval may indicate a less serious situation which would not warrant creating an alert.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Event rules, Processing Events, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Set a threshold to suppress alert generation

The event threshold is the rate upon which Event Management generates an alert. Receiving multiple events for a device over a short interval may warrant creating an alert, as the condition may be serious. However, receiving events over a longer interval may indicate a less serious situation which would not warrant creating an alert.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

You can configure the properties in an event rule to create alerts, suppress alert generation, or close existing alerts according to a specified threshold. The threshold is based on the value of event fields or number of occurrences over a specified period.

**Note:** **Field Name** can be the name of any numeric field in the **Additional information** field of the event. Therefore, if `CPU` is an additional information field for a specific event, then `CPU` can be used as a **Field Name**.

Assume that you want to generate an alert when CPU utilization reaches or exceeds 80% three times with no more than 20 seconds between any two consecutive events. Create an event rule with these settings \(an explanation for each value is given in parentheses\):

-   **Create Alert Operator**: **&gt;=** \(operator to determine whether utilization of **Field Name** reaches or exceeds the specified value\)
-   **Field Name**: **CPU** \(events regarding high CPU usage\)
-   **Threshold Value**: **80** \(percent\)
-   **Occurs**: **3** \(three events occur where the CPU usage is at or above "&gt;=" 80%\)
-   **Over\(seconds\)**: **20** \(20 seconds or less between events\)

To demonstrate how the preceding settings are evaluated, assume that the following events are received:

<table id="table_z4f_42z_2gb"><thead><tr><th>

Scenario

</th><th>

Outcome

</th></tr></thead><tbody><tr><td>

Reported elapsed time and the CPU usage for each event:

-   First event elapse time 20, CPU=85
-   Second event elapse time 40, CPU=80
-   Third event elapse time 60, CPU=70

</td><td>

In this scenario, no alert is generated since one event has a CPU utilization that is under 80%.

</td></tr><tr><td>

Reported elapsed time and the CPU usage for each event:

-   First event elapse time 20, CPU=85
-   Second event elapse time 40, CPU=90
-   Third event elapse time 70, CPU=95

</td><td>

In this scenario, an alert is not generated since the elapsed time in one event is over the specified 20 seconds.

</td></tr><tr><td>

Reported elapsed time and the CPU usage for each event:

-   First event elapse time 20, CPU=85
-   Second event elapse time 40, CPU=95
-   Third event elapse time 60, CPU=90

</td><td>

In this scenario, an alert is generated since in all events the elapsed time is within the specified time and the CPU usage is over 80%.

</td></tr></tbody>
</table>**Note:**

-   When configuring an event rule to create or close alerts according to a threshold, events that arrive at the same second, as determined by the **time\_of\_event** field, are skipped. This occurs because these events are considered to be duplicates.
-   When threshold conditions are configured, alerts close when the **Close Alert Operator** condition is met, and not when an event is received with **Severity = Clear** or **Resolution state = Closing**.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Rules** &gt; **Event Rules**.

2.  Create or open an event rule.

3.  Click **Threshold**.

4.  Select **Active**.

    If **Active** is not selected, the fields on this page do not appear.

5.  In the **Create Alert Operator** field, select an operator.

    -   If you select **Count**, specify the corresponding **Occurs** and **Over\(seconds\)** fields.
    -   If you select any operator other than **Count**, the **Field name** and **Threshold value** fields appear. Specify the required values in these fields.

        **Note:** The value of the **Threshold value** property can be the name of any field in the **Additional information** of the event. For example, if `CPU` is a field in **Additional information** for a specific event, then `CPU` can be used as the **Threshold value**.

    -   In the **Occurs** field, specify the required value.
    -   In the **Over\(seconds\)** field, specify the required period.
6.  To automatically close alerts, in the **Close Alert Operator** field, select an operator.

    Extra fields appear according to your selection.

    -   If **Count** is specified as the operator for the **Create Alert Operator** field, then the selection in the **Close Alert Operator** field is either `None` or `Idle`. Specify the required value.
    -   If you select **Idle**, configure the **Over\(seconds\)** field.
    -   In the **Close Alert Operator** field, if you select an operator other than **Idle**, then configure the **Threshold value**, **Occurs**, and **Over\(seconds\)** fields.
7.  Click **Save** or **Submit**.


## Example

To create an alert when a specific event occurs 5 times in 10 minutes, in **Threshold**:

1.  In the **Field name** field, specify the name of any field that exists in the **Additional information** field in the event. The value of the field is irrelevant.
2.  In the **Create Alert Operator** field, select `Count`.
3.  In the **Occurs** field, specify `5`.
4.  In the **Over** field, `600` \(10 \* 60 seconds\).
5.  Click **Save** or **Submit**.

To create an alert when a specific event occurs 5 times in 10 minutes with a metric value greater than 55. Assume that “metric\_value” is a field in the **Additional information** of the event. Specify:

1.  Select the **Active** check box.
2.  In the **Create Alert Operator** field, select `>=`.
3.  In the **Field name** field, specify **metric\_value**.
4.  In the **Threshold value** field, specify `55`.
5.  In the **Occurs** field, specify `5`.
6.  In the **Over** field, specify `600` \(10 \* 60 seconds\).
7.  Click **Save** or **Submit**.

**Parent Topic:**[Event rules](../concept/create-event-rules.md)

**Related topics**  


[Create or edit an event rule](create-or-edit-event-rule.md)

[Use event input information](../concept/event-input-information.md)

[Configure an event rule to customize alert content](t_EMComposeOuput.md)

[Filter the events that an event rule applies to](t_EMCreateFilter.md)

