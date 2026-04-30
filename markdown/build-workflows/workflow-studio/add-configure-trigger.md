---
title: Add and configure a trigger in a playbook
description: Begin building your playbook by adding and configuring the trigger.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Triggers, Building playbooks, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Add and configure a trigger in a playbook

Begin building your playbook by adding and configuring the trigger.

## Before you begin

Role required: playbook.admin or pd\_author

Review [Triggers](../concept/process-automation-designer-triggers.md).

[Create a trigger definition](create-trigger-definition.md) if needed.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio** &gt; **Playbooks** &gt; ****.

2.  Select the view you want to build in.

    The builder displays in **Diagram view** by default, but you can select **Board view** to switch views. Switch between views anytime as you build your playbook.

    ![View toggle button](../images/board-view.png)

3.  Open the configuration modal for the trigger.

    |View|Steps|
    |----|-----|
    |**Diagram**|Select the trigger to choose the record operation that fires this playbook.|
    |**Board**|Open the **More actions menu** \(![More actions menu](../images/icon-horizontal-menu.png)\) and select **Properties**.|

4.  **Note:** The playbook cannot be activated without a trigger, and you will see an error in the notification tray.

    Under the **Schedule** tab, choose how you want the playbook to be triggered.

    -   **Define your own conditions for when your process runs**: If you want to create your own custom conditions for when your playbook should run, select this option, choose a trigger type, and then select **Set your trigger conditions**. On the next screen, select a **Table** to trigger your playbook and the **Conditions** that cause your playbook to run. Finally, you can choose to run your trigger on [Table extension and classes](https://www.servicenow.com/docs/access?context=table-extension-and-classes&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US). When you're done adding conditions to your trigger, click **Done**.
    -   **Choose an existing trigger**: If you want to use a trigger that has all the conditions you need for your playbook, select this option. Then, choose an existing trigger from the list and select **Done**.
    **Note:** Playbooks can be triggered off of any table that the customer is entitled to use.

    The trigger is configured.


## What to do next

[Add and configure your stages.](add-configure-stage.md)

**Parent Topic:**[Triggers](../concept/process-automation-designer-triggers.md)

**Related topics**  


[Create a trigger definition](create-trigger-definition.md)

