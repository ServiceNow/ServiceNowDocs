---
title: Create an alert variable for an alert rule in RPA Hub
description: Create a variable to configure the messages of an alert rule.Use the Alert variable form to create a variable for an alert rule message configuration.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Alert rule and variable, Use, RPA Hub, Workflow Data Fabric]
---

# Create an alert variable for an alert rule in RPA Hub

Create a variable to configure the messages of an alert rule.

## Before you begin

You must do this task in the classic environment.

Create an alert rule. For more information, see [Create an alert rule to generate custom notifications in RPA Hub](create-alert-rule-rpa.md#).

Role required: sn\_rpa\_fdn.rpa\_support\_user, sn\_rpa\_fdn.rpa\_developer, or sn\_rpa\_fdn.rpa\_admin

## About this task

Alert variable refers to a variable or parameter associated with alerts of RPA Hub. It serves as a dynamic token within alert messages, and its value can be linked to a table's field or determined through conditional scripting.

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **Monitor** &gt; **Alert Rules**.

2.  Open an alert rule that you want to create and associate an alert variable to.

3.  In the Alert Variables related list, select **New**.

4.  On the form, fill in the fields.

5.  Select **Submit**.


**Parent Topic:**[Alert rule and variable in RPA Hub](../concept/alert-rule-rpa-hub.md)

## Alert variable form in RPA Hub

Use the Alert variable form to create a variable for an alert rule message configuration.

<table id="table_pyx_mhd_4qb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Variable Name

</td><td>

Name of the alert variable.

</td></tr><tr><td>

Alert Rule

</td><td>

Name of the alert rule.

</td></tr><tr><td>

Index

</td><td>

Order of the alert variables in the message.Default sort order for alert variables is ascending order.

</td></tr><tr><td>

Is Scripted

</td><td>

Option to verify the usability of the script. This option adds an advanced data fetch script.

</td></tr><tr><td>

Is Threshold value

</td><td>

Option to verify the usability of the threshold value.

</td></tr><tr><td>

Table

</td><td>

Field that indicates the table that is selected for this alert variable.For example, the bot process.

</td></tr><tr><td>

Field

</td><td>

Field of the table to be mapped.For example, the name of the bot process.

</td></tr><tr><td>

Script

</td><td>

Text field that accepts JavaScript code input and provides controls, such as syntax checking and formatting.For example, to return a value that is data for an alert variable, enter `data` as follows:

```
      return { value: data}; 
```

.

 This field appears when the **Is Scripted** option is selected.

</td></tr></tbody>
</table>