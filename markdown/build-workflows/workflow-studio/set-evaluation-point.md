---
title: Set variant evaluation point
description: Set a point in your base playbook after which the variants are evaluated and run.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Playbook variants, Understanding the playbook components, Build Playbooks, Playbooks, Workflow Studio, Build workflows]
---

# Set variant evaluation point

Set a point in your base playbook after which the variants are evaluated and run.

## Before you begin

Role required: admin or playbook.admin

## About this task

Instead of evaluating the variants at the start of your playbook, you can choose to evaluate variants after certain activities are complete in the base playbook. For example, in a recruitment playbook, you can run different variants such as Manager, Senior Manager, or Individual Contributor, based on the candidate profile or interview feedback during one of the stages. This gives you more flexibility in designing and building your playbook.

If you do not specify any evaluation point, the variants are evaluated at the start of the playbook based on the trigger conditions.

To insert an evaluation point, make sure that:

-   The playbook does not have any variant activity before the evaluation point.
-   Any prior activity does not overwrite the value of the evaluation point.
-   The variant condition does not refer to any activity after the point.

## Procedure

1.  Navigate to **All** &gt; **Workflow Studio**.

2.  Open your playbook with variants.

3.  In Diagram view, select **+** after the activity where you want to evaluate the variants.

4.  From the mini-picker, select the variants icon \(![](../images/playbook-variants-icon.png)\) to add variant evaluation point.

    ![Inserting a variant evaluation point.](../images/playbook-variant.png)

5.  To move the evaluation point to a different location:

    1.  Select the evaluation point.

        ![Variant evaluation point.](../images/playbook-evaluation-point.png)

    2.  On the Move the global variants evaluation point dialog box, select one of the following.

    |Option|Description|
    |------|-----------|
    |**Evaluate all variants at the beginning of the playbook**|Moves the evaluation point to the beginning of the playbook.|
    |**Evaluate children after field**|Displays a list of valid locations in the playbook and moves the evaluation point to the selected location.|


## What to do next

Test the playbook to make sure that it's working as expected. See, [Test a playbook](test-process.md)

**Parent Topic:**[Playbook variants](../concept/playbook-variants.md)

