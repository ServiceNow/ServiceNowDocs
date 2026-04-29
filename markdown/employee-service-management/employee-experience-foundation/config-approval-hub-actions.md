---
title: Configure actions
description: Using the action framework, configure actions and associate a set of actions as action groups for use in the different contexts.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Action framework, Setup task management, Configuring Employee Center, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Configure actions

Using the action framework, configure actions and associate a set of actions as action groups for use in the different contexts.

## Before you begin

Role required: sp\_admin or sn\_hr\_sp.esc\_admin

## About this task

Action items provide quick access to actions that you perform in various contexts. You can modify the actions to suit your business needs. For example, you can use the default approve or reject actions to process the requests directly from the approvals page.

## Procedure

1.  Navigate to **All** &gt; **Employee Center** &gt; **Action framework** &gt; **Actions**.

2.  Click **New** or edit an existing record.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Action label|Name of the action label that appears on the button.|
    |Action type|Select the action type from the available list.|
    |Active|Check the box to activate the action|
    |Action icon|Icon of the action.|
    |Table|Name of the table to which the action is associated. When a record from this table is open, this list action appears. For approvals, select sysapproval\_approver.|

4.  Click **Save** or **Update**.

5.  On the **Action parameters** related list, click **New** or edit an existing record.

6.  On the form, fill in the fields.

<table id="id_apm_rzw_mwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Action parameter name

</td><td>

Name of the action parameter.

</td></tr><tr><td>

Parameter type

</td><td>

Select the parameter type from the available list such as JSON, string, or reference.

</td></tr><tr><td>

Is client parameter

</td><td>

Check the box to use the parameters in the client script.

</td></tr><tr><td>

Is display value

</td><td>

Check the box to display the value. By default, the value in sn\_ex\_sp\_action\_parameter is set to false and is only visible in form if the parameter type is reference.-   When true, you get the display value of the field.
-   When false, you get the actual db value of the field.


</td></tr><tr><td>

Action parameter value

</td><td>

This option appears only when you select **string**. Parameter value in a string, for example **approved**

</td></tr><tr><td>

Table

</td><td>

Reference table to which this component is tied to. When a record from this table is open, this list action appears. For approvals, select sysapproval\_approver. This option appears only when you select **Reference**.

</td></tr><tr><td>

Field

</td><td>

Field from the table that you can select from the element tree such as **Sys ID**. This option appears only when you select **Reference**.

</td></tr><tr><td>

JSON parameter

</td><td>

JSON string you want to specify. For example, **\{"param": "value"\}**. This option appears only when you select **JSON**.

</td></tr></tbody>
</table>    In the OOTB actions,

    -   The **isEsignatureEnabled** value is **true** by default, the esignature approval authentication window appears.
    -   The **broadcastEventName** value broadcasts an event passed in the parameter to hide the buttons when esignature is successful to enable comments before the esignature scenario.
    **Note:** For custom actions, you can customize these two parameters.

7.  Select **Save** or **Update**.


## Result

Action is configured. You can combine a set of related action items as a group.

