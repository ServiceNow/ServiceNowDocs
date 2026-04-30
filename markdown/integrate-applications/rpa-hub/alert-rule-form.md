---
title: Alert rule form in RPA Hub
description: Use the Alert rule form to create an alert rule.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [RPA Hub reference, RPA Hub, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Alert rule form in RPA Hub

Use the Alert rule form to create an alert rule.

<table id="table_pyx_mhd_4qb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of the alert rule.

</td></tr><tr><td>

Active

</td><td>

Option to verify the usability of the alert rule.On clearing this option, the notifications will not be generated from this alert rule.

</td></tr><tr><td>

Application

</td><td>

Field that indicates which applications can use this alert rule.Role required to view this field: admin.

</td></tr><tr><td>

Alert Priority

</td><td>

Priority of the alert:-   **Critical**
-   **High**
-   **Medium**
-   **Low**

 The default value is set to **Medium**.

</td></tr><tr><td>

Alert Type

</td><td>

Type of alert:-   **Info**
-   **Warning**
-   **Error**

</td></tr><tr><td>

Description

</td><td>

Brief description of the alert rule.

</td></tr><tr><td class="sub-head" colspan="2">

Alert Trigger

</td></tr><tr><td>

Applies To

</td><td>

Table that the alert rule is applied on.For example, Bot Process \[cmdb\_ci\_rpa\_process\].

 Based on the table selected, after saving the record, a new related tab appears in the related list.

 For example, if you select a bot process related table in this field, the **Bot process** tab appears in the related list.

</td></tr><tr><td>

Trigger Type

</td><td>

Trigger type of the alert rule:-   **Check Periodically**: The alert rule is triggered periodically, based on the settings in the Time duration \(hours\) list.
-   **When something happens**: The alert rule is triggered when something happens on a record that is selected in the Applies to table.

For example, if **Bot process** is selected from the Applies To list, an alert rule is triggered when a record is updated in the bot process.


</td></tr><tr><td>

Time Duration \(hours\)

</td><td>

Frequency, in hours, at which the alert rule is triggered.For example, if **Bot process** is selected from the Applies To list, an alert rule is triggered when a record is updated in the bot process every **24** hours.

 This field appears only when **Check Periodically** is selected from the Trigger Type list.

</td></tr><tr><td>

Trigger Conditions

</td><td>

Conditions at which the alerts are triggered.Select a table from the Applies To list before modifying this field.

 Within the **Trigger Conditions** section, you can use the **Add Filter Condition** to add a trigger condition. For example, you might want to generate an alert rule when the life-cycle stage status of a bot process is not retired. In that case, select **Life Cycle Stage Status** from the – choose field – list, **is not** from the – oper – list, and **Retired** from the – value – list.

 ![Selected filter condition to trigger alert rule.](../image/alert-rule-trigger-conditions.png "Selected filter condition to trigger alert rule")

</td></tr><tr><td>

Apply Threshold

</td><td>

Option to verify the usability of the threshold.For example, if a **Process job** is selected from the Applies To list and a percentage or a number of process jobs fail in a given time period, to trigger an alert rule for the failure message, this option must be selected for the configuration of the threshold condition.

</td></tr><tr><td>

Threshold Type

</td><td>

Type of threshold:-   **Count**
-   **Percentage**

 This field appears only when the **Apply Threshold** option is selected.

</td></tr><tr><td>

Set Condition \(Threshold\)

</td><td>

Threshold conditions to trigger alerts.Select a table from the Applies To list before modifying this field.

 This field appears only when **Percentage** is selected from the Threshold Type list.

 For example, you might want to generate an alert rule when a percentage of process jobs fail in a given time period. In that case, select **Created** in the – choose field – list, **on** in the – oper – list, and **Today** in the – value – list.

 ![Set threshold condition to trigger alerts.](../image/alert-rule-set-condition.png "Set threshold condition to trigger alerts")

</td></tr><tr><td>

Comparison

</td><td>

Qualifier to trigger alerts:-   **Is equal to**
-   **Is less than**
-   **Is more than**
-   **Is less than or equal to**
-   **Is more than or equal to**

 This field appears only when the **Apply Threshold** option is selected.

</td></tr><tr><td>

Threshold Value

</td><td>

Value to determine if an alert rule must be triggered based on the qualifier selected in the **Comparison** field.For example, if a few process jobs fail in a day. To set a condition, select **Count** in the Threshold Type list, **Is more than** in the Comparison list, and **10** in the Threshold Value list.

 This field appears only when the **Apply Threshold** option is selected.

</td></tr><tr><td class="sub-head" colspan="2">

Alert Message

</td></tr><tr><td>

Message

</td><td>

Alert message.For example, `{0}% of process jobs failed in a day.`

 To configure the variables, such as \{0\}, see [Create an alert variable for an alert rule in RPA Hub](../task/create-alert-variable.md).

</td></tr><tr><td>

Send Email

</td><td>

Option to send an email notification of the alert message.

</td></tr><tr><td>

Users

</td><td>

Users who can receive the alert message email.This field appears only when you select the **Send Email** option.

</td></tr><tr><td>

Groups

</td><td>

Groups who can receive the alert message email.This field appears only when you select the **Send Email** option.

</td></tr></tbody>
</table>**Parent Topic:**[RPA Hub reference](rpa-hub-reference.md)

**Related topics**  


[Create an alert rule to generate custom notifications in RPA Hub](../task/create-alert-rule-rpa.md)

