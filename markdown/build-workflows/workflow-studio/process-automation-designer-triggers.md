---
title: Triggers
description: Triggers specify when to start running your playbook.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Building playbooks, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Triggers

Triggers specify when to start running your playbook.

In Playbooks, triggers indicate when your playbook should start running. Each trigger has a type and conditions that, when met, start running your activated playbook.

You can choose a trigger when you create a playbook in Workflow Studio. Start by adding a trigger, which defines the trigger type. Then, set conditions and other options to refine your trigger so that it fires in a way that makes sense for your business process. For more information, see [Create a process definition](../task/create-process-definition.md).

If there are no triggers that fit your use case, you can create your own trigger definition instead. For more information, see [Create a trigger definition](../task/create-trigger-definition.md).

![When the conditions specified in your trigger are met anywhere in the ServiceNow AI Platform, your automated playbook starts running.](../images/process-automation-designer-trigger-flow.png "How triggers work")

## Trigger types

In your Trigger Definition \[sys\_pd\_trigger\_definition\] record, you can choose a trigger type, which determines when your trigger fires. These trigger types represent record operations that can occur in the ServiceNow AI Platform®. The following trigger types are available in your instance by default:

-   **Record Created**

    The playbook runs when a user creates a record anywhere in the ServiceNow AI Platform.

-   **Record Updated**

    The playbook runs when a user updates an existing record anywhere in the ServiceNow AI Platform.

-   **Record Created or Updated**

    The playbook runs when a user creates a record or updates an existing record anywhere in the ServiceNow AI Platform.


**Note:** Triggers only fire for record operations that are interactive, or made by users. Triggers don't fire for non-interactive record operations. For more information, see [Non-interactive sessions](https://www.servicenow.com/docs/access?context=c_NonInteractiveSessions&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

## Conditions to run

After you add a trigger to your playbook, you can then set conditions and other options that determine when and how your trigger fires.

<table id="table_gcm_lhz_slb"><thead><tr><th>

Option

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Conditions

</td><td>

Use the condition builder to create field conditions for when your playbook runs. See [Condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

Run my process

</td><td>

Choose an option for when your playbook runs. Options include:-   **Once**: Triggers the playbook once for the life of the triggering input record.
-   **For each unique change**: Triggers the playbook for every unique update to a non-[system field](https://www.servicenow.com/docs/access?context=r_GlobalDefaultFields&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) even if the flow is currently running. The system stores a history of every change to a record and determines whether the change is unique. For example, if an incident record's **State** field changes from In Progress to On Hold, the playbook runs. However, if the **State** field then changes back to In Progress, the playbook doesn't run.

**Note:** Playbooks that have a trigger that runs **For each unique change** can produce recursions when run in a non-interactive session. When such playbooks make a change to the trigger record, the change meets the playbook's trigger conditions and causes a recursion.

-   **Only if not currently running**: Triggers the playbook for every unique change if a process execution is not currently running.
-   **For every update**: Triggers the playbook every time the input record is updated, regardless of whether there has already been or there currently are any running process executions.

</td></tr><tr><td>

Run on extended

</td><td>

Select this option to trigger the playbook on tables that extend from your selected table. For example, if you enable this option and select the Configuration Item \[cmdb\_ci\] table, your playbook runs when record operations occur on the Server \[cmdb\_ci\_server\], Computer \[cmdb\_ci\_computer\], and other extended tables. For more information, see [Table extension and classes](https://www.servicenow.com/docs/access?context=table-extension-and-classes&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

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

**Parent Topic:**[Building playbooks](building-a-process.md)

