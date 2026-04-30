---
title: Attended Configuration form in RPA Hub
description: Use the Attended Configurations form to associate the table form, from where the automation must be initiated, associate the respective attended bot process, and other related conditions.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, RPA Hub, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Attended Configuration form in RPA Hub

Use the Attended Configurations form to associate the table form, from where the automation must be initiated, associate the respective attended bot process, and other related conditions.

<table id="table_pyx_mhd_4qb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the attended configuration.

</td></tr><tr><td>

Bot Process Configuration

</td><td>

Select an attended bot process that executes the automation.Attended bot processes that aren’t retired and also have the **Enable Embedded Task Automation** option selected in the bot process form are displayed here.

</td></tr><tr><td>

Table

</td><td>

Select the table for the form, from where the automation \(bot process\) is triggered on. For example, Request \[sc\_request\]. Then the automation \(bot process\) is triggered from the Request form.

</td></tr><tr><td>

Action Label

</td><td>

Provide a label for the action \(UI button\) that the users would view on the associated table form.The value you entered in the **Name** field is the default value.

The Action Label must be unique for a table, in a particular domain, if the instance is domain separated.

</td></tr><tr><td>

Description

</td><td>

Brief description of the attended configuration.

</td></tr><tr><td class="sub-head" colspan="2">

Define TriggerProvide the criteria details that activate the action \(UI button\) on the associated table form that triggers bot process only when the following conditions are met. If criteria are not defined, automation can be triggered from all associated table forms.

</td></tr><tr><td>

Set Conditions

</td><td>

Define the criteria that activate the UI action on the associated table form that is selected in the **Table** field.Build a filter by adding conditions that contain a field, operator, and values. For example, to view the UI action when the associated form is active. In that case, select **Active** from the **Select field** list, **is** from the **Select operator** list, and **true** from the **Enter value** list.

Within the **Condition** section, you can use the **+New condition set** to add a new condition.

After you build a filter, select **Set**.

![A selected filter condition to activate the UI action.](../image/automation-trigger-cond-rpa.png "Example: Selected filter condition to activate the UI action")

</td></tr></tbody>
</table>**Parent Topic:**[RPA Hub reference](rpa-hub-reference.md)

**Related topics**  


[Create an attended configuration record in RPA Hub](../task/create-attended-config-rpa.md)

[Embedded Task Automation \(ETA\) in RPA Hub](../concept/embedded-task-auto-rpa.md)

[List of steps for configuring embedded task automation](list-steps-eta-rpa.md)

