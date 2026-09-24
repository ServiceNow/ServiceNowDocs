---
title: Scheduled jobs installed with Enterprise Architecture Workspace
description: The installation of the Enterprise Architecture Workspace store application adds scheduled jobs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-scheduled-jobs.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Enterprise Architecture Workspace reference, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Scheduled jobs installed with Enterprise Architecture Workspace

The installation of the Enterprise Architecture Workspace store application adds scheduled jobs.

<table id="table_w43_ssf_vzb"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Populate Technology Lifecycle Risks

</td><td>

Populates the TLM technology lifecycle risks data in the TLM Technology Lifecycle Risks \[sn\_apm\_tpm\_technology\_risk\] table.

</td></tr><tr><td>

Populate TPM Discovered Technologies and Lifecycles

</td><td>

Populates the technology lifecycle data in the TPM Technology Lifecycle \[sn\_apm\_tpm\_technology\_lifecycle\] table. The data includes end of support date, end of extended support date, and end of life date for your software and hardware models. **Note:** Software product data appears only when you have the Software Asset Management \(SAM\) Foundation or Software Asset Management \(SAM\) Professional plugin installed.

</td></tr><tr><td>

Populate TRM technical debts in the EA Workspace

</td><td>

Updates the Technical Debt \[sn\_apm\_trm\_standards\_technical\_debt\] table with the latest technical debt data for your application portfolio. Existing records persist across runs and move between Active, Resolved, and Archived states instead of being deleted and re-created. **Note:** The Populate TRM technical debts in the EA Workspace scheduled job appears only when you have the Software Asset Management \(SAM\) Foundation or Software Asset Management \(SAM\) Professional plugins installed.

</td></tr><tr><td>

Delete Archived Tech Debts

</td><td>

Runs automatically on the first day of every month and deletes Archived technical debt records whose **Updated** value is older than the retention period set in the system property **sn\_apm\_tpm.monthsToDeleteArchivedTechDebt**. The default retention period is 12 months. You can run this job manually to apply a retention period change immediately.

</td></tr><tr><td>

CSDM Product Model Assignment

</td><td>

Generates the Model ID for existing business applications with empty Model ID fields. An application model is a structured representation of a business application's components and their relationships and interactions within your application landscape.

</td></tr><tr><td>

Populate Number field in TPM Discovered Technologies

</td><td>

Populates missing Technology Lifecycle Management \(TLM\) lifecycle record identifiers for TPM Discovered Technology records created with TPM plugin versions earlier than 1.9.0.

</td></tr><tr><td>

Sync TRM Product Names with Software Products

</td><td>

Syncs the names of Technology Reference Model \(TRM\) products of type Software with the names of their linked Software Asset Management \(SAM\) software products in the TRM Products \[sn\_apm\_trm\_standards\_product\] table. This scheduled job is inactive by default and runs on demand.

</td></tr><tr><td>

Update Score Range in Indicator Score Table

</td><td>

Populates the TCO score range field on existing Indicator Score \[apm\_app\_indicator\_score\] records. Run this job on upgraded instances so the **Business applications by TCO score** widget on the **Portfolio TCO** dashboard displays TCO score bands instead empty state. The job is inactive by default and must be run on demand.

</td></tr></tbody>
</table>**Parent Topic:**[Enterprise Architecture Workspace reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-reference.md)

**Related topics**  


[Install Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/install-ea-workspace.md)

