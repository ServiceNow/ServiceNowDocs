---
title: Create a Data Definition
description: Use data definitions to collect and use pieces of information later in a playbook.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Administering playbooks, Configuring playbooks, Configuring Workflow Studio, Workflow Studio, Build workflows]
---

# Create a Data Definition

Use data definitions to collect and use pieces of information later in a playbook.

## Before you begin

**Important:** As of the 26.1 release, the **Collect user data** activity is no longer available in the activity picker. The activity will continue to function wherever it is used, but for new activities use the **Questionnaire** activity instead. The **Questionnaire** activity does not require you to create a data definition. To learn more about the **Questionnaire** activity, see [Questionnaire activity](../reference/questionnaire-activity.md).

Role required: admin, flow\_designer

You will be working in the ServiceNow AI Platform to complete this task.

## About this task

A data definition is the information that you want an agent or fulfiller to collect during a playbook run, and is the key input of the **Collect user data** activity. Playbook authors define the data they want an agent or fulfiller to collect in the `sys_flow_data_definition` table. When an agent or fulfiller collects the information, the information is stored in the `sys_flow_data` table for use later during the playbook run, instead of in the record table.

Only use a data definition if:

-   The data is only needed downstream during a single playbook run. It's collected, used, and never needed again.
-   You don't need to run any reports on the collected data. If you need any metrics or reports on the collected data, create a table and use the [User Form activity](../reference/user-form-activity.md) instead.

For example, you may have multiple teams that perform activities. One team enters the inputs for a created data definition when they perform a **Collect user data** activity, and then a second team uses the collected inputs to complete the playbook, and the information is not needed afterwards.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Process Automation Administration** &gt; **Data Definitions**.

2.  Select **New** to create a new data definition.

3.  Give your new data definition a name.

    **Note:** Data definitions have the same scope as other metadata tables, by default.

4.  Right-click in the record header to **Save**.

    If you select the **Submit** button, you are taken back to the **Data Definitions** list and will need to select your new data definition to re-open it.

5.  Add fields for information that you want an agent to collect.

    1.  In the **Flow Data Variables** table, select **New**.

    2.  Enter the required fields.

<table id="choicetable_qcs_vmh_j1c"><tbody><tr><td id="d89302e232">

**Type**

</td><td>

The type of input the agent is collecting for a field. For example, string, reference, integer, etc.

</td></tr><tr><td id="d89302e241">

**Label**

</td><td>

The label of the field in the UI, during the playbook run. The label can consist of any text.

</td></tr><tr><td id="d89302e253">

**Column name**

</td><td>

The name of the input being collected. Spaces cannot be used to delimit words.

</td></tr><tr><td id="d89302e262">

**Max Length**

</td><td>

The maximum length a string value can be entered for a string type of field. The variable can store longer strings than it can display.

</td></tr><tr><td id="d89302e271">

**Application**

</td><td>

The application scope for the data variable. It is always set to Global, and cannot be changed.

</td></tr></tbody>
</table>6.  Optional configurations
7.  Under the **Default Value** tab, specify the value used when a playbook does not provide a value.

8.  Right-click in the record header to **Save**.


## Result

The data definition can now be used when configuring activities in Playbooks in Workflow Studio.

## Example

During a playbook run, you can use data definitions to potentially:

-   Collect a shipping address, then reference the address when generating a shipping label.
-   Ask the user "yes" or "no" questions, and determine subsequent activities based on the user's responses.

## What to do next

Configure a [**Collect user data** activity](../reference/collect-user-data-activity.md) in Workflow Studio Playbooks to use your new data definition.

**Parent Topic:**[Administering playbooks](../concept/administering-process-automation-designer.md)

