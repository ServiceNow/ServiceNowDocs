---
title: Scheduled jobs for TLM in the EA Workspace
description: Several types of scheduled jobs are added for Technology Lifecycle Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-portfolio-management/eaw-tpm-scheduled-jobs.html
release: zurich
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Activate the Technology Lifecycle Management \(TLM\) plugin, Configure Technology Lifecycle Management, Configure EA Workspace using the Setup page, Configure, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Scheduled jobs for TLM in the EA Workspace

Several types of scheduled jobs are added for Technology Lifecycle Management.

**Important:**

Technology Lifecycle Management \(TLM\) was previously known as Technology Portfolio Management \(TPM\). TPM and TLM refer to the same feature. Table names and scheduled job names continue to use TPM and haven't been renamed.

Whether your instance displays TPM or TLM also depends on your application versions. TLM labels appear only when both the Enterprise Architecture Workspace application \(version 9.2.1 or later\) and the Technology Lifecycle Management plugin, sn\_apm\_tpm \(version 1.11.0 or later\), are installed. If either application is on an earlier version, the interface continues to show TPM.

The following is the list of scheduled jobs for Technology Lifecycle Management \(TLM\) in EA Workspace:

<table id="table_cqf_13p_k1c"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Populate TPM Technology Lifecycle Risks

</td><td>

Populates the TLM technology life-cycle risks data in the TPM Technology Life-cycle Risks \[sn\_apm\_tpm\_technology\_risk\] table.

</td></tr><tr><td>

Populate TPM Discovered Technologies and Lifecycles

</td><td>

Discovers technologies from CMDB and Service Mapping relationships and populates lifecycle milestone data for your software products and hardware models. The job creates records in the TPM Discovered Technologies \[sn\_apm\_tpm\_discovered\_technology\] table and then populates the TPM Technology Lifecycle \[sn\_apm\_tpm\_technology\_lifecycle\] table with end of support, end of extended support, and end of life dates. Lifecycle records are created as part of this job and not by standalone business rules. The job also displays a percentage complete indicator to help you track progress: technologies discovery accounts for 80%, removing invalid technologies for 10%, and populating lifecycle records for 20%. Lifecycle data for software products is available only when the Software Asset Management \(SAM\) Foundation or Software Asset Management \(SAM\) Professional plugin is activated.

**Important:** If you upgraded to the Australia release and the TPM Technology Lifecycle table is empty or not updating, run this scheduled job. In prior releases, lifecycle records were created by standalone asynchronous business rules. As of the Australia release, those business rules have been removed and lifecycle record creation is handled entirely by this scheduled job.

</td></tr><tr><td>

Populate TRM technical debts in the EA Workspace

</td><td>

Updates the Technical Debt \[sn\_apm\_trm\_standards\_technical\_debt\] table with the latest technical debt data for your software products that is available in the TPM Discovered Technology \[sn\_apm\_tpm\_discovered\_technology\] table.**Note:** The Populate TRM technical debts in the EA Workspace scheduled job will be available only the Software Asset Management \(SAM\) Foundation or Software Asset Management \(SAM\) Professional plugin is installed.

</td></tr></tbody>
</table>**Parent Topic:**[Activate the Technology Lifecycle Management \(TLM\) plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-install-tpm.md)

**Related topics**  


[Run a scheduled job to update TRM technical debt data in EA Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-run-job-trm-tech-debts.md)

[Update TLM data for a business application or application service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/update-tpm-data.md)

[Restart the TLM Discovered Technologies and Lifecycles job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-restart-tpm-scheduled-job.md)

