---
title: Add and configure a trigger in a playbook
description: Begin building your playbook by adding and configuring the trigger.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Triggers, Building playbooks, Use, Workflow Studio, Build workflows]
---

# Add and configure a trigger in a playbook

Begin building your playbook by adding and configuring the trigger.

## Before you begin

Role required: playbook.admin or pd\_author

Review [Triggers](../concept/process-automation-designer-triggers.md).

[Create a trigger definition](create-trigger-definition.md) if needed.

## About this task

You can add one or multiple triggers to your playbook. The triggers can either be record based or scheduled. Record based triggers start your playbook when a record is created, updated, or both. The scheduled triggers give you the option to run the playbook at the time you need. You can also add an existing trigger that matches the conditions for your playbook.

**Note:** You can create up to 10 triggers of any type. It can be record-based triggers, scheduled triggers, or a combination of both.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio** &gt; **Playbooks**.

2.  Open the playbook that you want to configure or create a playbook.

3.  On the left sidebar, select **Triggers** \(![Icon to open the triggers.)](../images/triggers-icon.png)\).

    **Note:** You can't open triggers until the parent table is specified for the playbook. To specify a parent table, edit **Start** in the diagram view, or open the **More actions menu** \(![More actions menu](../images/icon-horizontal-menu.png)\) and select **Properties**.

    ![Triggers in playbooks with options to edit, delete, or create triggers.](../images/triggers-playbook.png)

    If triggers are already added to the playbook, the **Triggers** screen displays a list of the associated triggers. You can edit, delete, or add a trigger.

4.  Select an existing trigger to edit, or add a trigger.

<table id="table_d5r_w4z_zfc"><thead><tr><th>

Trigger type

</th><th>

Actions

</th></tr></thead><tbody><tr><td>

Record based

</td><td>

Go to **Add trigger** &gt; **Record based** and select when you want the playbook to run:-   When record is created
-   When record is updated
-   When record is created or updated
If you want to specify a different table for the trigger than the parent table, use dot-walking to specify the relation between the two tables. You can choose to run your trigger on [Table extension and classes](https://www.servicenow.com/docs/access?context=table-extension-and-classes&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) or start your trigger only on unique change of records. After you specify the **Conditions** that should start your playbook, select **Save and close**.

If you want to use a trigger that has all the conditions you need for your playbook, select **Choose existing playbook trigger**. Then, choose an existing trigger from the list and select **Save and close**.

</td></tr><tr><td>

Scheduled

</td><td>

1.  Select **Add trigger** &gt; **Scheduled**.
2.  Specify the scheduling details and the conditions for the trigger and select **Save and close**.
For more information about scheduling a trigger, see [Create a scheduled trigger for playbook](create-scheduled-trigger-definition.md)

</td></tr></tbody>
</table>
## Result

The trigger is configured.

## What to do next

[Add and configure your stages.](add-configure-stage.md)

**Parent Topic:**[Triggers](../concept/process-automation-designer-triggers.md)

**Related topics**  


[Create a trigger definition](create-trigger-definition.md)

[Create a scheduled trigger for playbook](create-scheduled-trigger-definition.md)

