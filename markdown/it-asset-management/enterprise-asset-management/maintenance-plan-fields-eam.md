---
title: Maintenance plan fields for Enterprise Asset Management
description: A detailed description of all maintenance plan fields in the Enterprise Asset Management application.
locale: en-US
release: yokohama
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Enterprise Asset Management reference, Enterprise Asset Management, IT Asset Management]
---

# Maintenance plan fields for Enterprise Asset Management

A detailed description of all maintenance plan fields in the Enterprise Asset Management application.

## Maintenance Plan

|Field|Description|
|-----|-----------|
|Active|Option that indicates if the maintenance plan is active.|
|Name|Name of the maintenance plan.|
|Short description|Brief description of the maintenance plan.|

## Target Assets

<table id="table_r2v_f5w_cwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Target Enterprise Asset Management table that lists the enterprise assets that you want to apply the maintenance plan to. The default table is **Enterprise asset**.

</td></tr><tr><td>

Filter conditions

</td><td>

Filter conditions that enable you to apply the maintenance plan to only specific subsets of enterprise assets.

 You can add multiple filter conditions to a single maintenance plan using the following options:

-   **or**: Enables you to specify any of the conditions that an enterprise asset can meet to have the maintenance plan applied to it.
-   **and**: Enables you to specify all the conditions that an enterprise asset must meet to have the maintenance plan applied to it.
-   **+ New condition set**: Enables you to specify additional sets of conditions that an enterprise asset can meet to have the maintenance plan applied to it.

</td></tr><tr><td>

Apply to new matching records

</td><td>

Option to apply the maintenance plan to any subsequent enterprise assets that are added to the target Enterprise Asset Management table and meet the specified filter conditions.

</td></tr><tr><td>

Task creation policy

</td><td>

Policy that specifies what action you want to take when the maintenance plan is applied to an enterprise asset that is already under maintenance.

 Select one of the following options:

-   **Leave alone**: Prevents the creation of tasks for the new maintenance plan and the deletion of tasks that are associated with the existing maintenance plan.
-   **Cancel existing**: Deletes all tasks that are associated with the existing maintenance plan.
-   **Add to existing**: Adds both new tasks and existing active tasks to the new maintenance plan.

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

[Maintenance schedule fields for Enterprise Asset Management](maintenance-schedule-fields-eam.md)

[Work plan fields for Enterprise Asset Management](wp-fields-eam.md)

[Work plan schedule fields for Enterprise Asset Management](work-plan-schedule-fields-eam.md)

[Expense line fields for Enterprise Asset Management](expense-line-fields-eam.md)

[Fields inherited from a parent asset group to a sub group](subgroups-parent-fields-eam.md)

[Enterprise asset disposal order stages](eamasset-disposalorder-stages.md)

[Terminology for linear assets](terms-eam.md)

[Installed with Enterprise Asset Management for Healthcare](installed-with-eam-healthcare.md)

[Installed with OT Asset Management](installed-with-otam.md)

[Components installed with Enterprise Asset Management for Data Center and Network Asset Management \(DCNAM\)](installed-with-eam-dcnam.md)

[Components installed with Enterprise Asset Management for Providers](installed-with-eam-providers.md)

[Scheduled jobs and tables installed with normalization of firmware models](firmware-tables-jobs-ot.md)

[Asset put away task fields](put-away-task-form-eam.md)

