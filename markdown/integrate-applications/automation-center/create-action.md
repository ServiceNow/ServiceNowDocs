---
title: Create an action
description: Create an action to view and execute in Action Center to fix issues that cause automations to fail in Automation Center.
locale: en-US
release: australia
product: Automation Center
classification: automation-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Creating an action, Working with actions, Use, Automation Center, Workflow Data Fabric]
---

# Create an action

Create an action to view and execute in Action Center to fix issues that cause automations to fail in Automation Center.

## Before you begin

Role required: sn\_ac.automation\_technical\_user and sn\_ac.automation\_admin

## Procedure

1.  Navigate to **All** &gt; **Automation Center** &gt; **Build** &gt; **Actions**.

2.  Select **New**.

3.  On the Action Details form, fill in the fields.

<table id="table_wgg_bww_fbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique number that is auto-populated.

</td></tr><tr><td>

Application

</td><td>

Scope of the action.

</td></tr><tr><td>

Name

</td><td>

Intuitive name for the action.

</td></tr><tr><td>

Category

</td><td>

Select an action category that you want to associate with the action.

</td></tr><tr><td>

Type

</td><td>

Select the type of action category that you want to associate with the action.

</td></tr><tr><td>

Action Type

</td><td>

The type of action that is created in Flow designer. The available values are **Flow/Subflow** and **Action**.

</td></tr><tr><td>

Action

</td><td>

The action that you have created in Flow Designer.**Note:** You cannot map one flow, subflow, or action created in Flow Designer to multiple actions in Automation Center.

</td></tr><tr><td>

Active

</td><td>

This is a non-editable field.

</td></tr><tr><td>

Enable concurrent executions

</td><td>

Select this option if you want to execute the same action concurrently in Action Center.

</td></tr><tr><td>

Description

</td><td>

Description of the action.

</td></tr><tr><td>

Execution instructions

</td><td>

Any execution instructions that you want to provide.

</td></tr></tbody>
</table>4.  Select **Submit** to save the action.

5.  Select **Activate** only if there are no more changes expected for the associated action.

    If you select **Activate**, you cannot make any other changes to the action configuration, that is the **Action Type** and **Action** fields. The other fields can be updated.


**Parent Topic:**[Creating an action](../concept/creating-action.md)

