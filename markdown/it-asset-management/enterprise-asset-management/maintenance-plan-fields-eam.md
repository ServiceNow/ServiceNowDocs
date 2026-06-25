---
title: Maintenance plan fields for Enterprise Asset Management
description: A detailed description of all maintenance plan fields in the Enterprise Asset Management application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/enterprise-asset-management/maintenance-plan-fields-eam.html
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: reference
last_updated: "2026-03-12"
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
</table>**Parent Topic:**[Enterprise Asset Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/reference-enterprise-asset-management.md)

**Related topics**  


[Domain separation and Enterprise Asset Management]()

[Components installed with Enterprise Asset Management]()

[OT Asset Workspace roles]()

[Asset fields for enterprise assets]()

[Asset audit fields for enterprise assets]()

[Audit results]()

[Enterprise model categories and corresponding classes]()

[Mandatory fields in the bulk import spreadsheets]()

[Normalization status for enterprise models]()

[Model fields for Enterprise Asset Management]()

[Contract fields for Enterprise Asset Management]()

[Maintenance schedule fields for Enterprise Asset Management]()

[Work plan fields for Enterprise Asset Management]()

[Work plan schedule fields for Enterprise Asset Management]()

[Expense line fields for Enterprise Asset Management]()

[Fields inherited from a parent asset group to a sub group]()

[Enterprise asset disposal order stages]()

[Terminology for linear assets]()

[Scheduled jobs and tables installed with normalization of firmware models]()

[Asset put away task fields]()

