---
title: Work plan fields for Enterprise Asset Management
description: A detailed description of all work plan fields in the Enterprise Asset Management application.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Enterprise Asset Management reference, Enterprise Asset Management, IT Asset Management]
---

# Work plan fields for Enterprise Asset Management

A detailed description of all work plan fields in the Enterprise Asset Management application.

## Work Plan

<table id="table_ukh_f5w_cwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique number for the work plan.

</td></tr><tr><td>

Name

</td><td>

Name of the work plan.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the work plan.

</td></tr><tr><td>

Effective start

</td><td>

Effective start date from when the work plan is active.

</td></tr><tr><td>

Effective end

</td><td>

Effective end date until when the work plan is active.

</td></tr><tr><td>

Active

</td><td>

Option that indicates if the work plan is available to use.

</td></tr><tr><td>

Forecast work orders

</td><td>

Option to specify if this work plan is applicable to estimate and generate the upcoming work orders.

 If this option is selected, you can view the **Generate work orders** option by selecting the **More Actions** ellipsis icon. This generates a work order for the schedule per asset.

</td></tr></tbody>
</table>## Conditions

<table id="table_r2v_f5w_cwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Target Enterprise Asset Management table that the work plan is associated with. The default table is **Enterprise asset**.

</td></tr><tr><td>

Category

</td><td>

Determine whether the work plan is applicable for either category: original equipment scheduling \(OEM\) or alternative equipment scheduling \(AEM\).

</td></tr><tr><td>

Apply to new matching records

</td><td>

Option to apply the work plan to any subsequent enterprise assets that are added to the target Enterprise Asset Management table and meet the specified filter conditions.

</td></tr><tr><td>

Task creation policy

</td><td>

Specify what to do when a work plan runs based on a schedule occurrence that is already in progress.

 Select one of the following options:

-   **Leave alone**: Prevents the creation of tasks for the new work plan and the deletion of tasks that are associated with the existing work plan.
-   **Cancel existing**: Deletes existing tasks associated with the plan and creates tasks to replace them.
-   **Add to existing**: Allows new tasks to replace the existing active tasks for the specific schedule occurrence of a plan.

</td></tr><tr><td>

Filter conditions

</td><td>

Filter conditions that enable you to apply the work plan to specific subsets of enterprise assets.

 You can add multiple filter conditions to a single work plan using the following options:

-   **or**: Enables you to specify any of the conditions that an enterprise asset can meet to have the maintenance plan applied to it.
-   **and**: Enables you to specify all the conditions that an enterprise asset must meet to have the maintenance plan applied to it.
-   **+ New condition set**: Enables you to specify additional sets of conditions that an enterprise asset can meet to have the maintenance plan applied to it.

</td></tr></tbody>
</table>**Parent Topic:**[Enterprise Asset Management reference](../concept/reference-enterprise-asset-management.md)

**Related topics**  


[Domain separation and Enterprise Asset Management](../concept/domain-separation-eam.md)

[Enterprise Asset Management roles](eam-roles.md)

[OT Asset Workspace roles](ot-workspace-roles.md)

[Asset fields for enterprise assets](asset-fields-eam.md)

[Asset audit fields for enterprise assets](asset-audit-record-fields-eam.md)

[Audit results](audit-results-eam.md)

[Enterprise model categories and corresponding classes](enterprise-model-categories.md)

[Mandatory fields in the bulk import spreadsheets](mandatory-bulk-fields.md)

[Normalization status for enterprise models](norm-status-eam.md)

[Model fields for Enterprise Asset Management](eam-model-fields.md)

[Contract fields for Enterprise Asset Management](contract-fields-eam.md)

[Maintenance plan fields for Enterprise Asset Management](maintenance-plan-fields-eam.md)

[Maintenance schedule fields for Enterprise Asset Management](maintenance-schedule-fields-eam.md)

[Work plan schedule fields for Enterprise Asset Management](work-plan-schedule-fields-eam.md)

[Expense line fields for Enterprise Asset Management](expense-line-fields-eam.md)

[Fields inherited from a parent asset group to a sub group](subgroups-parent-fields-eam.md)

[Enterprise asset disposal order stages](eamasset-disposalorder-stages.md)

[Terminology for linear assets](terms-eam.md)

[Scheduled jobs and tables installed with normalization of firmware models](firmware-tables-jobs-ot.md)

[Asset put away task fields](put-away-task-form-eam.md)

