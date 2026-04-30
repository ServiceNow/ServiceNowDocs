---
title: Create Security Operations workflow triggers
description: Create a workflow trigger that contains a condition on a table.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Security Operations workflow triggers, Security Operations common functionality, Security Operations]
---

# Create Security Operations workflow triggers

Create a workflow trigger that contains a condition on a table.

## Before you begin

Security Operations contains several workflow triggers in the base system:

-   **Configuration item changes on an active Security Incident**

    Uses integration to enrich CI-related data as configuration items change.

-   **Rescan vulnerable group**

    Rescans a vulnerable group, using the [Scan vulnerability workflow](../../vulnerability-response-orchestration/task/scan-vulnerability-workflow.md), when you **Close/Ignore** the group.

-   **Rescan vulnerable item**

    Rescans a vulnerable item, using the [Scan vulnerability item workflow](../../vulnerability-response-orchestration/task/scan-vulnerable-item-workflow.md) when you **Close/Ignore** the item.


Roles required:

-   To read: sn\_sec\_cmn.read
-   To create or update: sn\_sec\_cmn.write
-   To delete: sn\_sec\_cmn.admin

## Procedure

1.  Navigate to **All** &gt; **Security Operations** &gt; **Utilities** &gt; **Workflow Triggers**.

2.  Click **New**.

3.  Fill in the fields on the form, as appropriate.

<table id="table_vks_thr_ns"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the workflow trigger.

</td></tr><tr><td>

Description

</td><td>

Enter a description for the workflow trigger.

</td></tr><tr><td>

Table

</td><td>

The table containing the workflow trigger. If you selected the **Use filter group** check box and selected a filter group, this field defaults to the table associated with the selected filter group.

</td></tr><tr><td>

Condition

</td><td>

Use the [condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US) to define the criteria for the workflow trigger. If you selected the **Use filter group** check box and selected a filter group, the **Condtion** fields are not displayed.

</td></tr><tr><td>

Active

</td><td>

Select this check box to activate the workflow trigger.

</td></tr><tr><td>

Use filter group

</td><td>

Select this check box to use a predefined filter group or [create a new filter group](create-filter-group.md) to define the workflow trigger criteria.

</td></tr><tr><td>

Filter group

</td><td>

Select the filter group to use for defining workflow triggers. This field appears only if the **Use filter groups** check box is selected.

</td></tr></tbody>
</table>4.  When you have completed your entries, right-click in the form header and select **Save**.

    ![WorkflowTriggers with filters example](../image/WorkflowTriggerFilters.png)

    The **Workflows** tab appears. It contains workflows that are run when all filter conditions or filter group conditions are met.

5.  To add workflows, perform these steps.

    1.  In the **Workflows** tab, click **Edit**.

    2.  Use the condition builder, if needed, to locate the workflows you want to select, or use the slushbucket to select workflows and move them to the Workflows List.

    3.  Click **Save**.

    The selected workflows are added.

6.  Click **Update**.


**Parent Topic:**[Security Operations workflow triggers](../concept/workflow-triggers.md)

