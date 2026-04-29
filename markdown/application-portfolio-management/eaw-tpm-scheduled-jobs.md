---
title: Scheduled jobs for TPM in the EA Workspace
description: Several types of scheduled jobs are added for Technology Portfolio Management.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Activate the Technology Portfolio Management \(TPM\) plugin, Configure Technology Portfolio Management, Configure EA Workspace using the Setup page, Configuring Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Scheduled jobs for TPM in the EA Workspace

Several types of scheduled jobs are added for Technology Portfolio Management.

The following is the list of scheduled jobs for Technology Portfolio Management \(TPM\) in EA Workspace:

<table id="table_cqf_13p_k1c"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Populate TPM Technology Lifecycle Risks

</td><td>

Populates the TPM technology life-cycle risks data in the TPM Technology Life-cycle Risks \[sn\_apm\_tpm\_technology\_risk\] table.

</td></tr><tr><td>

Populate TPM Discovered Technologies and Lifecycles

</td><td>

Populates the technology life-cycle data in the TPM Technology Lifecycle \[sn\_apm\_tpm\_technology\_lifecycle\] table. The data includes end of support date, end of extended support date, and end of life date for your software products and hardware models.**Note:** The data for software products is displayed only when the Software Asset Management \(SAM\) Foundation or Software Asset Management \(SAM\) Professional plugin.

</td></tr><tr><td>

Populate TRM technical debts in the EA Workspace

</td><td>

Updates the Technical Debt \[sn\_apm\_trm\_standards\_technical\_debt\] table with the latest technical debt data for your software products that is available in the TPM Discovered Technology \[sn\_apm\_tpm\_discovered\_technology\] table.**Note:** The Populate TRM technical debts in the EA Workspace scheduled job will be available only the Software Asset Management \(SAM\) Foundation or Software Asset Management \(SAM\) Professional plugin is installed.

</td></tr></tbody>
</table>**Parent Topic:**[Activate the Technology Portfolio Management \(TPM\) plugin](../../task/eaw-task/eaw-install-tpm.md)

**Related topics**  


[Run a scheduled job to update TRM technical debt data in EA Workspace](../../task/eaw-task/eaw-run-job-trm-tech-debts.md)

[Schedule a job to generate TPM lifecycle data](../../task/schedule-job-generate-tpm-data.md)

[Schedule a job to generate TPM technology risk](../../task/schedule-job-generate-tpm-risk.md)

