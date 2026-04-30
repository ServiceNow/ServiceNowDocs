---
title: Expense line fields for Enterprise Asset Management
description: A detailed description of all expense line fields in the Enterprise Asset Management application.
locale: en-US
release: yokohama
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Enterprise Asset Management reference, Enterprise Asset Management, IT Asset Management]
---

# Expense line fields for Enterprise Asset Management

A detailed description of all expense line fields in the Enterprise Asset Management application.

## Expense Line

<table id="table_b21_dgr_fwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique number that is used to identify and track the expense line. This field populates automatically.

</td></tr><tr><td>

Date

</td><td>

Date on which you are creating the expense line. This field is automatically set to the current date.

</td></tr><tr><td>

Inherited

</td><td>

Option that indicates if the expense line is inherited from a parent expense line.If you enable this option, the **Parent** field appears below the **Inherited** field. In the **Parent** field, search for and select the parent expense line that this expense line is inherited from. The following fields are then inherited from the parent expense line and can no longer be modified:

-   **Source ID**
-   **Asset**
-   **Contract**
-   **User**
-   **Configuration Item**
-   **Task**
-   **Cost center**

</td></tr><tr><td>

Source ID

</td><td>

Enterprise asset that you want to associate with the expense line. Based on the enterprise asset that you select, the corresponding fields in the Source form section populate automatically.

</td></tr><tr><td>

Amount

</td><td>

Cost of the enterprise asset that you want to associate with the expense line. To indicate that you have received a credit towards the enterprise asset, enter a negative number.**Note:** You can set this field to any currency of your choice.

</td></tr><tr><td>

Process date

</td><td>

Date and time at which the expense line is processed.

</td></tr><tr><td>

State

</td><td>

State of the expense line.

</td></tr><tr><td>

Summary type

</td><td>

Expense line category. Select one of the following options:-   **Grow Business**: Expense lines for enterprise assets that are used to help your business grow.
-   **Run Business**: Expense lines for enterprise assets that are used to help your business run.
-   **Transform Business**: Expense lines for enterprise assets that are used to help transform your business.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the expense line.

</td></tr></tbody>
</table>## Source

<table id="table_st2_cjw_4tb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Asset

</td><td>

Enterprise asset that you want to associate with the expense line.

</td></tr><tr><td>

Fixed asset

</td><td>

Fixed asset that contains the selected enterprise asset.A fixed asset is a container that holds one or more individual assets. If the enterprise asset that you selected in the **Asset** field is contained within a fixed asset, the **Fixed asset** field populates automatically.

</td></tr><tr><td>

Contract

</td><td>

Contract that the selected enterprise asset is associated with.

</td></tr><tr><td>

User

</td><td>

User who the selected enterprise asset is assigned to.

</td></tr><tr><td>

Configuration item

</td><td>

Configuration item \(CI\) that is associated with the expense line.

</td></tr><tr><td>

Task

</td><td>

Task that is associated with the expense line.

</td></tr><tr><td>

Cost center

</td><td>

Cost center that is financially responsible for the selected enterprise asset.

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

[Work plan fields for Enterprise Asset Management](wp-fields-eam.md)

[Work plan schedule fields for Enterprise Asset Management](work-plan-schedule-fields-eam.md)

[Fields inherited from a parent asset group to a sub group](subgroups-parent-fields-eam.md)

[Enterprise asset disposal order stages](eamasset-disposalorder-stages.md)

[Terminology for linear assets](terms-eam.md)

[Installed with Enterprise Asset Management for Healthcare](installed-with-eam-healthcare.md)

[Installed with OT Asset Management](installed-with-otam.md)

[Components installed with Enterprise Asset Management for Data Center and Network Asset Management \(DCNAM\)](installed-with-eam-dcnam.md)

[Components installed with Enterprise Asset Management for Providers](installed-with-eam-providers.md)

[Scheduled jobs and tables installed with normalization of firmware models](firmware-tables-jobs-ot.md)

[Asset put away task fields](put-away-task-form-eam.md)

