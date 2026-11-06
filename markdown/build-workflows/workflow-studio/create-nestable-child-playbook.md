---
title: Create a nestable child playbook
description: Nest a child playbook within a parent playbook to organize your processes. Creating child playbooks that can be used in other parent playbooks enables you to define sets of activities that can be re-used across multiple playbooks to avoid duplication.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/build-workflows/workflow-studio/create-nestable-child-playbook.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-10-16"
reading_time_minutes: 3
breadcrumb: [Nested Playbooks, Playbooks patterns, Playbooks, Workflow Studio, Build workflows]
---

# Create a nestable child playbook

Nest a child playbook within a parent playbook to organize your processes. Creating child playbooks that can be used in other parent playbooks enables you to define sets of activities that can be re-used across multiple playbooks to avoid duplication.

## Before you begin

Role required: admin, playbook.admin, or playbook.write

## About this task

The child playbook must be activated to display as an option for selection in the parent playbook. After the child playbook is created, you must define at least one launch playbook permission for the child playbook to be activated.

**Note:** Nested \(child\) playbook must have the same runtime permissions as the parent.

To define a launch playbook permission for the child playbook:

1.  Select the Start node in the diagram view of the playbook or open the Process Properties from the overflow menu.
2.  Select **Runtime Permissions** &gt; **Add a Permission Set**.
3.  Define some permission criteria and then select the **Trigger on-demand** check box.
4.  Select **Save and close**.

## Procedure

1.  Navigate to **All** &gt; **Workflow Studio** &gt; **Playbooks**.

2.  In the workspace window, select **New** &gt; **Playbook**.

3.  In the **New Playbook** window:

    1.  Make sure that **Standard playbook** is selected as the **Type**.
    2.  Enter a **Playbook name**.
    3.  Enter a **Description** that helps you identify the playbook.
    4.  Select an **Application** scope.
    5.  Select **Standalone** for the **Execution type**:

        \[Omitted image "create-standalone-playbook.png"\] Alt text: Playbook user interface that shows how to select the Standalone option.

        When you select **Standalone**, the option **Allow this playbook to be nest-able in another playbook** automatically appears and is selected.

    6.  Select **Build playbook**.
4.  In the Diagram view of the playbook you just created, select the plus sign between **Start** and **End**, and then select **Create a stage to put your activities in**.

5.  Select the stage to define the stage details and runtime permissions in the properties panel.

    For more information, see [Stages and activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/process-automation-designer-lanes-activities.md).

6.  Select the **Start** node, and then on the **Inputs &amp;Outputs** tab, add the inputs that the parent playbook passes to the child and the outputs that the child returns to the parent.

    For more information about playbook inputs, see [Create a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/create-process-definition.md).

    1.  Select **Add input** or **Add output**.

    2.  Enter a **Label**.

        The **Name** is generated from the label and can't be edited.

    3.  Select a **Type**.

    4.  For an input, turn on **Mandatory** if the parent playbook must supply a value.

    5.  Expand the item to set its remaining properties.

        A String item has **Hint**, **Default value**, and **Max length**. A Reference item has **Hint**, **Reference table**, and **Reference qualifier**.

7.  In the stage, add a **Set Playbook Outputs** activity.

8.  Select the **Set Playbook Outputs** activity, then the **Automation** tab, and define the outputs that the child returns to the parent playbook.

    The outputs that you added on the **Inputs &amp; Outputs** tab appear under **Playbook Outputs** at the bottom of the **Automation** tab.

9.  In the **Diagram view** window, select **Activate**.

10. Select **Save and close**.

    For more information about creating a playbook, see [Create a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/create-process-definition.md).


## What to do next

After you successfully build the nestable child playbook and activate it, build the parent playbook to host the nestable child playbook. See [Create a parent playbook to host a nestable child playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/create-parent-playbook.md).

