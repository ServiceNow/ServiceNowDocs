---
title: Alert variable form in RPA Hub
description: Use the Alert variable form to create a variable for an alert rule message configuration.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, RPA Hub, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Alert variable form in RPA Hub

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
</table>**Parent Topic:**[RPA Hub reference](rpa-hub-reference.md)

**Related topics**  


[Create an alert variable for an alert rule in RPA Hub](../task/create-alert-variable.md)

