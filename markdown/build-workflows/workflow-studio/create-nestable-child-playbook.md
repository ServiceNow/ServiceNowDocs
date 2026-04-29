---
title: Create a nestable child playbook
description: Nest a child playbook within a parent playbook to organize your processes. Creating child playbooks that can be used in other parent playbooks enables you to define sets of activities that can be re-used across multiple playbooks to avoid duplication.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Nested Playbooks, Design Playbook Experience, Playbooks, Workflow Studio, Build workflows]
---

# Create a nestable child playbook

Nest a child playbook within a parent playbook to organize your processes. Creating child playbooks that can be used in other parent playbooks enables you to define sets of activities that can be re-used across multiple playbooks to avoid duplication.

## Before you begin

Role required: admin, playbook.admin, or playbook.write

## About this task

The child playbook must be activated to display as an option for selection in the parent playbook. After the child playbook is created, you must define at least one launch playbook permission for the child playbook to be activated.

To define a launch playbook permission for the child playbook:

1.  Select the Start node in the diagram view of the playbook or open the Process Properties from the overflow menu.
2.  Select **Runtime Permissions** &gt; **Add a Permission Set**.
3.  Define some permission criteria and then select the **Trigger on-demand** check box.
4.  Select **Save**.

## Procedure

1.  Navigate to **All** &gt; **Workflow Studio**.

2.  In the workspace window, select **New** &gt; **Playbook**.

3.  In the **New Playbook** window:

    1.  Make sure that **Standard playbook** is selected as the **Type**.
    2.  Enter a **Playbook name**.
    3.  Enter a **Description** that helps you identify the playbook.
    4.  Select an **Application** scope.
    5.  Select **Standalone** for the **Execution type**:

        ![Playbook user interface that shows how to select the Standalone option.](../images/create-standalone-playbook.png)

        When you select **Standalone**, the option **Allow this playbook to be nest-able in another playbook** automatically appears and is selected.

    6.  Select **Build playbook**.
4.  In the Diagram view of the playbook you just created, select the plus sign between **Start** and **End**, and then select **Create a stage to put your activities in**.

5.  Define the stage properties in the panel.

6.  In the window, select **Activate**.

7.  Select **Save and close**.

    For more information about creating a playbook, see [Create a playbook](create-process-definition.md).


## What to do next

After you have successfully built the nestable child playbook and activated it, build the parent playbook to host the nestable child playbook. See [Create a parent playbook to host a nestable child playbook](create-parent-playbook.md).

