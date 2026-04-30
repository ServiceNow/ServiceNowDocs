---
title: Create a custom identification type for Password Reset
description: A custom identification type enables the user to enter alternative verification information such as an employee ID while resetting the password.
locale: en-US
release: zurich
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Customizing Password Reset processes, Configure, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a custom identification type for Password Reset

A custom identification type enables the user to enter alternative verification information such as an employee ID while resetting the password.

## Before you begin

Role required: password\_reset\_admin

## About this task

## Procedure

1.  Navigate to **All** &gt; **Password Reset** &gt; **Extensions** &gt; **Identification Types**.

2.  Click **New**, enter a unique and meaningful **Name** and **Description**, and then fill in the form.

<table id="table_npc_gdz_f1b"><tbody><tr><td>

Identification field label

</td><td>

Text to display as a label for the **Identification** field.

</td></tr><tr><td>

Identification processor

</td><td>

Identification processor script. Choose an existing script or create your own using the Identification form processor category \(extension script\).

</td></tr></tbody>
</table>3.  Click **Submit**.


**Parent Topic:**[Customizing Password Reset processes](../concept/customizing-password-reset.md)

**Related topics**  


[Create a Password Reset extension script](t_CreateAnExtensionScript.md)

