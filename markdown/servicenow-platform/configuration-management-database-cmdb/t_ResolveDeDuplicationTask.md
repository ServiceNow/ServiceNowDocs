---
title: Review de-duplication tasks \(manual\)
description: Review details of de-duplication tasks which remediate duplicate CIs, and then potentially process a de-duplication task.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Duplicate CIs remediation, CMDB data management, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Review de-duplication tasks \(manual\)

Review details of de-duplication tasks which remediate duplicate CIs, and then potentially process a de-duplication task.

## Before you begin

Role required: sn\_cmdb\_editor or itil to view, and sn\_cmdb\_admin, itil\_admin, or cmdb\_dedup\_admin to remediate a de-duplication task.

## About this task

Alternatively, you can use de-duplication capabilities in CMDB Workspaceor in Service Graph Workspace. Use the De-duplication dashboard and the De-duplication Template Library to:

-   Review de-duplication tasks
-   Process de-duplication tasks in bulk by using de-duplication templates
-   Gain insights into de-duplication counts and status in your organization

For more information, see [CI de-duplication experience in CMDB Workspace and in Service Graph Workspace](../concept/dedup-ci-exp-cmdb-workspace.md).

If a duplicate CI is a dependent CI, then you can view the details of the dependent relationship, the Depend on CI, and any relation qualifier chain. If the dependent CI has a lookup table, then you can see the details of the respective lookup table.

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **Identification/Reconciliation** &gt; **De-duplication Tasks**.

2.  Select a task.

<table id="table_eqy_xbr_3s"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique task number.

</td></tr><tr><td>

Assigned to

</td><td>

Person who is responsible for resolving the task.

</td></tr><tr><td>

Short description

</td><td>

Description for the task.

</td></tr><tr><td>

Work notes

</td><td>

Details describing how the CI was identified as a duplicate.

**Note:** Not available in de-duplication tasks that were created prior to the London release.

 This field also contains user notes about the decisions and steps of resolving the task.

</td></tr><tr><td>

Priority

</td><td>

Task priority.

</td></tr><tr><td>

State

</td><td>

State of the de-duplication task as it progresses through resolution.

</td></tr></tbody>
</table>3.  In the related lists section, click the **Duplicate Audit Results** tab to see the list of duplicate CIs in this task. You can click a CI to display more CI details.

<table id="table_ng3_kgn_js"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Duplicate CI

</td><td>

Reference to the duplicate CI. **Note:** This field is a document ID type, which means that it can reference any record on any table. If the referenced CI is deleted as part of resolving duplicate tasks, then this field is empty.

</td></tr><tr><td>

Relationship

</td><td>

For a duplicate CI that is a dependent CI, this field shows the relationship between the duplicate CI and depend on CI.

</td></tr><tr><td>

Depend on CI

</td><td>

If the duplicate CI is a dependent CI, then this field displays the depend on CI.

</td></tr><tr><td>

Discovery source

</td><td>

Discovery method used for the CI.

</td></tr></tbody>
</table>
## What to do next

Analyze de-duplication tasks to determine which CIs should remain active and which of the duplicate CIs in the Duplicate Audit Results lists are stale or incorrect. Select **Remediate** to [remediate a single de-duplication task](reconcile-dup-task.md).

**Parent Topic:**[Duplicate CIs remediation](../concept/de-duplication-tasks.md)

**Related topics**  


[Relation qualifier](../concept/c_RelationQualifier.md)

[bundle-platadm.t_CreatingADocumentIDField]

