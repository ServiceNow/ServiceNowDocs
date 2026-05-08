---
title: Triggers
description: Triggers specify when to start running your playbook.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Understanding the playbook components, Build Playbooks, Playbooks, Workflow Studio, Build workflows]
---

# Triggers

Triggers specify when to start running your playbook.

In Playbooks, triggers indicate when your playbook should start running. Each trigger has a type and conditions that, when met, start running your activated playbook.

You choose one or more triggers when you create a playbook in Workflow Studio. To add a trigger, start by choosing the trigger type. Then, set conditions and other options to refine your trigger so that it fires in a way that makes sense for your business process. Repeat if you want your playbook to run based on multiple triggers. For more information, see [Create a process definition](../task/create-process-definition.md).

**Note:** You can also configure and activate a playbook without any trigger, if you're planning to only trigger the playbook via API.

If you don't see a trigger that fits your use case, you can also create your own trigger definition instead. For more information, see [Create a trigger definition](../task/create-trigger-definition.md).

## Trigger types

In your Trigger Definition \[sys\_pd\_trigger\_definition\] record, you can choose a trigger type, which determines when your trigger fires. These trigger types represent record operations that can occur in the ServiceNow AI Platform®. The following trigger types are available in your instance by default:

-   **Scheduled**

    The playbook runs on a schedule specified by the playbook author.

-   **When record is created**

    The playbook runs when a user creates a record anywhere in the ServiceNow AI Platform.

-   **When record is updated**

    The playbook runs when a user updates an existing record anywhere in the ServiceNow AI Platform.

-   **When record is created or updated**

    The playbook runs when a user creates a record or updates an existing record anywhere in the ServiceNow AI Platform.


**Note:** Triggers only fire for record operations that are interactive, or made by users. Triggers don't fire for non-interactive record operations. For more information, see Non-interactive sessions.

## Details

After you add a trigger to your playbook, you can then set conditions and other options that determine when and how your trigger fires.

<table id="table_gcm_lhz_slb"><thead><tr><th>

Option

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Conditions

</td><td>

Use the condition builder to create field conditions for when your playbook runs. See Condition builder.

</td></tr><tr><td>

Run this trigger on extended tables

</td><td>

Select this option to trigger the playbook on tables that extend from your selected table. For example, if you enable this option and select the Configuration Item \[cmdb\_ci\] table, your playbook runs when record operations occur on the Server \[cmdb\_ci\_server\], Computer \[cmdb\_ci\_computer\], and other extended tables. For more information, see Table extension and classes.

</td></tr><tr><td>

Trigger on unique change

</td><td>

Select this to trigger the playbook for every unique update to a non-system field even if the flow is currently running. The system stores a history of every change to a record and determines whether the change is unique. For example, if an incident record's **State** field changes from In Progress to On Hold, the playbook runs. However, if the **State** field then changes back to In Progress, the playbook doesn't run.**Note:** Playbooks that have a trigger that runs **For each unique change** can produce recursions when run in a non-interactive session. When such playbooks make a change to the trigger record, the change meets the playbook's trigger conditions and causes a recursion.

</td></tr></tbody>
</table>## Design considerations

Refer to these design considerations when working with triggers:

-   **Create unique filter conditions for record triggers on the same table**

    To prevent playbooks from overwriting each other, create unique filter conditions for each playbook that runs on the same table. If multiple playbooks on the same table have the same filter, there is no way to know the order in which the playbooks will run.

-   **Avoid duplicating triggers used in Workflow Studio flows**

    Playbooks triggers do not override Workflow Studio triggers. For both applications, when the trigger conditions are met, the automated processes run.

-   **Ignore records added or updated by import and update sets**

    Record triggers ignore records that were added or updated by applying an update set or importing an XML file. These operations apply to the entire application or table instead of an individual record.


-   **[Create a trigger definition](../task/create-trigger-definition.md)**  
Define the type of trigger that determines when to start running your playbook.
-   **[Add and configure a trigger in a playbook](../task/add-configure-trigger.md)**  
Begin building your playbook by adding and configuring the trigger.
-   **[Create a scheduled trigger for Playbook](../task/create-scheduled-trigger-definition.md)**  
Create a scheduled trigger that starts your playbook at the required time and interval. You can schedule a trigger in any time zone, with or without an end date for the schedule.

**Parent Topic:**[Understanding the playbook components](playbook-building-blocks.md)

