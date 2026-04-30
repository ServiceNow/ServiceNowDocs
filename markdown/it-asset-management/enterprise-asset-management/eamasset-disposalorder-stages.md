---
title: Enterprise asset disposal order stages
description: An enterprise asset disposal order goes through various stages in the disposal process before it’s completed. With each stage, the task that's associated with that stage changes too.
locale: en-US
release: yokohama
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Enterprise Asset Management reference, Enterprise Asset Management, IT Asset Management]
---

# Enterprise asset disposal order stages

An enterprise asset disposal order goes through various stages in the disposal process before it’s completed. With each stage, the task that's associated with that stage changes too.

Closing a task in the asset disposal process completes that task and automatically creates the next task in the process. For example, after you close the Schedule Pickup task, the state for that task changes to Closed Complete and the next task, Asset Departure, is created. This process continues until you close all the tasks required for disposing of the selected assets. After you close all the tasks, the disposal order is completed.

|Enterprise disposal stages|Task|Description|
|--------------------------|----|-----------|
|Draft|Verify Assets|Asset disposal record is created.|
|Scheduling|Schedule Pickup|Scheduling details for the asset disposal order.|
|Transit|Asset Departure|Verified assets are ready for departure.|
|Confirmation|Vendor Confirmation|Asset disposal order is confirmed by the vendor.|
|Documentation|Disposal Documentation|Documentation for the disposal record is attached.|
|Completed|None|Asset disposal record request is completed.|
|Cancelled|None|Disposal order can be canceled only until the transit stage.|

**Parent Topic:**[Enterprise Asset Management reference](../concept/reference-enterprise-asset-management.md)

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

[Expense line fields for Enterprise Asset Management](expense-line-fields-eam.md)

[Fields inherited from a parent asset group to a sub group](subgroups-parent-fields-eam.md)

[Terminology for linear assets](terms-eam.md)

[Installed with Enterprise Asset Management for Healthcare](installed-with-eam-healthcare.md)

[Installed with OT Asset Management](installed-with-otam.md)

[Components installed with Enterprise Asset Management for Data Center and Network Asset Management \(DCNAM\)](installed-with-eam-dcnam.md)

[Components installed with Enterprise Asset Management for Providers](installed-with-eam-providers.md)

[Scheduled jobs and tables installed with normalization of firmware models](firmware-tables-jobs-ot.md)

[Asset put away task fields](put-away-task-form-eam.md)

