---
title: Components installed for duplicate CI remediation
description: Tables installed to support duplicate CI remediation \(included in the com.snc.cmdb plugin\).
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Duplicate CIs remediation, CMDB data management, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Components installed for duplicate CI remediation

Tables installed to support duplicate CI remediation \(included in the com.snc.cmdb plugin\).

## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Remediate Duplicate Task\[reconcile\_duplicate\_task\]

</td><td>

De-duplication tasks.

</td></tr><tr><td>

Duplicate Audit Result\[duplicate\_audit\_result\]

</td><td>

CIs associated with each de-duplication task.

</td></tr><tr><td>

Duplicate CI Remediation\[cmdb\_duplicate\_ci\_remediation\]

</td><td>

Input, selections on each tab, overall status of remediation, and results of each run of the Duplicate CI Remediator.

</td></tr><tr><td>

CMDB Workspace De-duplication template library\[sn\_cmdb\_ws\_reconcile\_duplicate\_template\_library\]

</td><td>

Library names and their descriptions.

</td></tr><tr><td>

De-duplication template suggested task\[sn\_cmdb\_ws\_reconcile\_duplicate\_template\_suggested\_task\]

</td><td>

Mappings of de-duplication tasks to templates.

</td></tr></tbody>
</table>## Scheduled jobs installed

<table id="table_wjk_shx_4zb"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

De-duplication: Populate Duplicate Task Data

</td><td>

Runs daily to copy metadata, such as the identification attributes and identification rules used in generating a de-duplication task, into an easily accessible table. The metadata is stored in the Reconcile Duplicate Task Data \[reconcile\_duplicate\_task\_data\] table and used for analytics for the De-duplication dashboard.

</td></tr><tr><td>

De-duplication: Populate Template Task Run Records

</td><td>

Runs every minute to evaluate the de-duplication tasks applicable for a template according to your settings. Based on settings, assigns matching tasks and manually added tasks to the template for remediation.

 De-duplication tasks are remediated after you select **Run template**.

</td></tr><tr><td>

De-Duplication: Template Scheduler

</td><td>

Runs every minute by the template scheduler to check the capacity of the execution engine. If there is available capacity, picks any new de-duplication tasks added to the queue, for remediation.

 De-duplication tasks aren't remediated and remain in ready state unless this job runs periodically.

</td></tr><tr><td>

De-duplication: Populate Template Suggested and Orphan Tasks

</td><td>

Runs hourly to count the number of tasks that match each published template and the number of tasks that don’t match any published template. These counts then appear on various cards in the De-duplication dashboard.

</td></tr></tbody>
</table>**Parent Topic:**[Duplicate CIs remediation](../concept/de-duplication-tasks.md)

