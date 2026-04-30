---
title: Scheduled jobs and tables installed with normalization of firmware models
description: Scheduled jobs that run during the normalization of firmware models embedded into Operational Technology \(OT\) assets and tables that store firmware normalization details are installed with the OT Asset Management application.
locale: en-US
release: yokohama
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Enterprise Asset Management reference, Enterprise Asset Management, IT Asset Management]
---

# Scheduled jobs and tables installed with normalization of firmware models

Scheduled jobs that run during the normalization of firmware models embedded into Operational Technology \(OT\) assets and tables that store firmware normalization details are installed with the OT Asset Management application.

<table id="table_knc_ytj_tdc"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Firmware Content Upload

</td><td>

-   Uploads data from the firmware tables to the CDS Client Staging \[cds\_client\_staging\] table.
-   Skips the upload if Content Data Service \(CDS\) hasn’t pulled all data.
-   Uses the Firmware configuration \[sn\_itam\_firmware\_configuration\] table to identify the firmware tables from which the content should be pushed.
-   Skips the upload if normalization hasn't run after the latest pull.

</td></tr><tr><td>

Firmware Content File Manager

</td><td>

Triggers during on-premise content import and export actions.

</td></tr><tr><td>

Firmware – Daily Job

</td><td>

-   Sets the time when the data is pulled by the Content Data Service \(CDS\).
-   Sets current life-cycle phase of model life cycles.

</td></tr><tr><td>

Firmware – Apply latest content changes

</td><td>

Processes changes in the content tables after content pull.

</td></tr><tr><td>

Firmware - Generate Lifecycles

</td><td>

Updates firmware model records with the recently updated content life-cycle details. This is a weekly job.

</td></tr><tr><td>

Firmware Normalization

</td><td>

Normalizes firmware models using the newly downloaded content.

</td></tr></tbody>
</table>|Table|Description|
|-----|-----------|
|Firmware model normalization \[sn\_itam\_firmware\_model\_norm\]|Stores the normalization rule and hash used to perform normalization of firmware models.|
|Firmware product \[sn\_itam\_firmware\_product\]|Stores firmware product records.|
|Custom firmware product \[sn\_itam\_cust\_firmware\_product\]|Stores custom firmware product records.|
|Firmware product version \[sn\_itam\_firmware\_product\_version\]|Stores firmware product version records.|
|Custom firmware product version \[sn\_itam\_cust\_firmware\_product\_version\]|Stores version records of custom firmware products.|
|Firmware publisher \[sn\_itam\_firmware\_publisher\]|Stores firmware publisher records.|
|Custom firmware publisher \[sn\_itam\_cust\_firmware\_publisher\]|Stores custom firmware publisher records.|
|Firmware lifecycle definition \[sn\_itam\_firmware\_lifecycle\_def\]|Stores the life-cycle phase of firmware models. Also stores the start and end date of each life-cycle phase.|
|Firmware model lifecycle \[sn\_itam\_firmware\_model\_lifecycle\]|Stores life-cycle definitions of firmware models.|
|Firmware normalization map \[sn\_itam\_firmware\_norm\_mapping\]|Stores the hash values that are used to normalize discovered firmware models.|
|Firmware CPE mapping \[sn\_itam\_firmware\_cpe\_mapping\]|Stores details of mapping between firmware and CPE.|
|Custom firmware CPE mapping \[sn\_itam\_cust\_firmware\_cpe\_mapping\]|Stores custom firmware and CPE mapping details.|
|Firmware content audit \[sn\_itam\_firmware\_content\_audit\]|Stores content values that changed.|
|Manage firmware library \[sn\_itam\_firmware\_manage\_library\]|Stores import and export content data.|
|Firmware configuration \[sn\_itam\_firmware\_configuration\]|Stores opt-in and opt-out data.|

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

[Enterprise asset disposal order stages](eamasset-disposalorder-stages.md)

[Terminology for linear assets](terms-eam.md)

[Installed with Enterprise Asset Management for Healthcare](installed-with-eam-healthcare.md)

[Installed with OT Asset Management](installed-with-otam.md)

[Components installed with Enterprise Asset Management for Data Center and Network Asset Management \(DCNAM\)](installed-with-eam-dcnam.md)

[Components installed with Enterprise Asset Management for Providers](installed-with-eam-providers.md)

[Asset put away task fields](put-away-task-form-eam.md)

