---
title: Enterprise Asset Management roles
description: The following roles help you to configure and use the Enterprise Asset Management application to manage the life cycle of your assets, parts, and their hierarchical relationships.
locale: en-US
release: yokohama
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Enterprise Asset Management reference, Enterprise Asset Management, IT Asset Management]
---

# Enterprise Asset Management roles

The following roles help you to configure and use the Enterprise Asset Management application to manage the life cycle of your assets, parts, and their hierarchical relationships.

After access has been granted to a role, all the groups or users assigned to the role are granted the access. Roles can contain other roles, and any access granted to a role is granted to any role that contains it.

## Enterprise Asset Management roles

<table id="table_o23_ynl_xsb"><thead><tr><th>

Role title

</th><th>

Contains roles

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enterprise asset manager

 \[sn\_eam.enterprise\_asset\_manager\]

</td><td>

-   wm\_initiator
-   sn\_eam.enterprise\_mobile\_user
-   sn\_eam.enterprise\_asset\_creator
-   sn\_eam.enterprise\_asset\_technician
-   sn\_eam.asset\_manager
-   inventory\_user
-   contract\_manager
-   procurement\_user
-   cmdb\_query\_builder
-   cmdb\_read
-   plan\_maint\_admin
-   wm\_task\_initiator

</td><td>

This role has access to all Enterprise Asset Management features except administrative functions.

</td></tr><tr><td>

Enterprise admin

 \[sn\_eam.enterprise\_admin\]

</td><td>

-   inventory\_admin
-   catalog\_manager
-   report\_user
-   sn\_eam.enterprise\_asset\_manager
-   asset
-   procurement\_admin
-   sn\_ent.classification\_manager
-   sn\_otam.ot\_asset\_manager

</td><td>

This role has full access to the Enterprise Asset Management application as well as the OT Asset Workspace.

</td></tr><tr><td>

Enterprise technician \[enterprise\_asset\_technician\]

</td><td>

-   sn\_eam.enterprise\_mobile\_user
-   sn\_eam.enterprise\_asset\_editor
-   sn\_ent.classification\_reader
-   canvas\_user

</td><td>

This role is for users who perform work tasks and update asset records as part of the asset lifecycle. This role has access to the following enterprise asset tasks: -   all RMA tasks except the Prepare task
-   all recall tasks
-   all disposal tasks
-   all loaner tasks except the Prepare task
-   enterprise asset audit
-   lease-end Collection, Preparation, and Shipment tasks

</td></tr><tr><td>

Enterprise mobile user

 \[sn\_eam.enterprise\_mobile\_user\]

</td><td>

none

</td><td>

This role has access to scan assets from a mobile application as well as dispose assets from a mobile application.

</td></tr><tr><td>

Agent\[wm\_agent\]

</td><td>

none

</td><td>

This role is for users who perform work on enterprise assets and record details in the corresponding work orders and work order tasks.**Note:** The wm\_agent role must contain an additional role such as enterprise\_asset\_manager, enterprise\_asset\_technician, or any other role to log into the Enterprise Asset Workspace.

</td></tr></tbody>
</table>**Parent Topic:**[Enterprise Asset Management reference](../concept/reference-enterprise-asset-management.md)

**Related topics**  


[Domain separation and Enterprise Asset Management](../concept/domain-separation-eam.md)

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

