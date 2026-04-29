---
title: ValidateTableChange
description: The ValidateTableChange validator reports any activities in the workflow that are invalid given the table associated with the workflow version.
locale: en-US
release: australia
product: Legacy Workflow
classification: legacy-workflow
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Workflow validator, Workflow validation, Workflow management, Classic Workflow, Build workflows]
---

# ValidateTableChange

The **ValidateTableChange** validator reports any activities in the workflow that are invalid given the table associated with the workflow version.

For example, a workflow version that is associated with the Change Request \[change\_request\] table but has a **Catalog Request** activity on the canvas is invalid, since the activity is not compatible with the selected table.

## Validation summary

-   Risk: If the current record at runtime does not originate from the table specified by the lowest common table, the activities for the lowest common table cannot set specific values.
-   Severity Level: Warning if the table that is associated with a workflow is higher in the table hierarchy than the lowest common table required for the workflow activities.
-   Valid Result: Valid
-   Valid Message: All activities are valid for the newly selected table
-   Invalid Result: Invalid Activity
-   Invalid Message: This workflow contains &lt;count of invalid activities&gt; invalid activities for the newly selected table.
-   Suggested Action: Make one of these changes:
    -   Change the workflow to not require the activities associated with the lowest table reported.
    -   Modify the workflow to use a table that contains the lowest common table in its hierarchy.
    -   Ensure that the current record meets the requirements of the at-risk activities.
-   Publishable: Yes
-   Runnable: Yes
-   Related Information: [Workflow activities](../../using-workflows/concept/c_WorkflowActivities.md)

## Troubleshooting

Navigate to **Workflow** &gt; **Administration** &gt; **Activity Definitions**. Note the **Table** column in the list. Each activity that is not global is associated with a table.

When you select a table in the Workflow Properties form, the activity menu presents only activities that are compatible with the selected table. Associating a table with a workflow activity enables the system to make certain decisions about the activity that affect value comparison, condition routing, or the setting and getting of field values in the current record.

When a workflow is set to the Global \[global\] table, it is possible that the process executing the workflow ensures that the current record meets the requirements of the activities identified by this validator. In that case, the activity still works as expected. If that assurance cannot be guaranteed by the user process, do not use the activity identified by the validator without assigning a table that meets the requirements of all the activities on the canvas.

This validation check ensures that the table specified by all the activities in a particular workflow is included in the hierarchy of the table selected for the workflow.

**Parent Topic:**[Workflow validator](r_WorkflowValidator.md)

