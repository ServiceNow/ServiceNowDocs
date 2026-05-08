---
title: Create a trigger definition
description: Define the type of trigger that determines when to start running your playbook.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Triggers, Understanding the playbook components, Build Playbooks, Playbooks, Workflow Studio, Build workflows]
---

# Create a trigger definition

Define the type of trigger that determines when to start running your playbook.

## Before you begin

-   Make sure to set your current application to the application that you want your playbook to run in. For more information, see Application picker.
-   Role required: admin, playbook.admin, or pd\_trigger\_author

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Process Automation Administration** &gt; **Trigger Definitions**.

2.  In the context header, click **New**.

3.  On the Trigger Definition form, in the **Label** field, enter any label for your trigger definition.

    This label appears as a trigger option when you [Create a playbook](create-process-definition.md).

4.  Next to the **Trigger Type** field, click the lookup using list icon \(![Lookup using list icon](../../flow-designer/images/lookup-using-list-icon.png)\).

5.  In the Trigger Types list, select a trigger type to use for your trigger definition.

    Options include:

    -   **Record Created**

        The playbook runs when a user creates a record anywhere in the ServiceNow AI Platform.

    -   **Record Updated**

        The playbook runs when a user updates an existing record anywhere in the ServiceNow AI Platform.

    -   **Record Created or Updated**

        The playbook runs when a user creates a record or updates an existing record anywhere in the ServiceNow AI Platform.

6.  Click **Next** to go on to the next step.

7.  In the Table list, select a table whose record operations you want to trigger your playbook.

8.  Under Condition, use the condition builder to add field conditions for when you want to trigger your playbook.

9.  To trigger your playbook for tables that extend your selected table, select the **Run On Extended** check box.

    For more information, see Table extension and classes.

10. Click **Update** to finish creating your trigger definition.


## Result

Your trigger definition is added to the Trigger Definition \[sys\_pd\_trigger\_definition\] table. You can now select your preset trigger when you [Create a playbook](create-process-definition.md).

**Parent Topic:**[Triggers](../concept/process-automation-designer-triggers.md)

**Related topics**  


[Add and configure a trigger in a playbook](add-configure-trigger.md)

[Create a scheduled trigger for Playbook](create-scheduled-trigger-definition.md)

