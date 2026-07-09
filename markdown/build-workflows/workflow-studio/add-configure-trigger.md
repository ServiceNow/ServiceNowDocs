---
title: Add and configure a trigger in a playbook
description: Begin building your playbook by adding and configuring the trigger.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/build-workflows/workflow-studio/add-configure-trigger.html
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Triggers, Building playbooks, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Add and configure a trigger in a playbook

Begin building your playbook by adding and configuring the trigger.

## Before you begin

Role required: playbook.admin or pd\_author

Review [Triggers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/process-automation-designer-triggers.md).

[Create a trigger definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/create-trigger-definition.md) if needed.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio** &gt; **Playbooks** &gt; ****.

2.  Select the view you want to build in.

    The builder displays in **Diagram view** by default, but you can select **Board view** to switch views. Switch between views anytime as you build your playbook.

    \[Omitted image "board-view.png"\] Alt text: View toggle button

3.  Open the configuration modal for the trigger.

    |View|Steps|
    |----|-----|
    |**Diagram**|Select **Start** to choose the record operation that triggers this playbook.|
    |**Board**|Open the **More actions menu** \(\[Omitted image "icon-horizontal-menu.png"\] Alt text: More actions menu\) and select **Properties**.|

4.  **Note:** The playbook cannot be activated without a trigger, and you will see an error in the notification tray.

    Under the **Schedule** tab, choose how you want the playbook to be triggered.

    -   **Define your own conditions for when your process runs**: If you want to create your own custom conditions for when your playbook should run, select this option, choose a trigger type, and then select **Set your trigger conditions**. On the next screen, select a **Table** to trigger your playbook and the **Conditions** that cause your playbook to run. Finally, you can choose to run your trigger on [Table extension and classes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/table-extension-and-classes.md). When you're done adding conditions to your trigger, click **Done**.
    -   **Choose an existing trigger**: If you want to use a trigger that has all the conditions you need for your playbook, select this option. Then, choose an existing trigger from the list and select **Done**.
    **Note:** Playbooks can be triggered off of any table that the customer is entitled to use.

    The trigger is configured.


## What to do next

[Add and configure your stages.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/add-configure-stage.md)

**Parent Topic:**[Triggers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/process-automation-designer-triggers.md)

**Related topics**  


[Create a trigger definition]()

