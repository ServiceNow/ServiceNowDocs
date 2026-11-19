---
title: Scheduled jobs installed with Enterprise Architecture Workspace
description: Scheduled jobs are installed with the Enterprise Architecture Workspace store application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-scheduled-jobs.html
release: brazil
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Enterprise Architecture Workspace reference, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Scheduled jobs installed with Enterprise Architecture Workspace

Scheduled jobs are installed with the Enterprise Architecture Workspace store application.

<table id="table_w43_ssf_vzb"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**CSDM Product Model Assignment**

</td><td>

Generates the Model ID for existing business applications with empty Model ID fields. An application model is a structured representation of a business application's components and their relationships and interactions within your application landscape.

</td></tr><tr><td>

**Sync TRM Product Names with Software Products**

</td><td>

Syncs the names of Technology Reference Model \(TRM\) products of type Software with the names of their linked Software Asset Management \(SAM\) software products in the TRM Products \[sn\_apm\_trm\_standards\_product\] table. This scheduled job is inactive by default and runs on demand. To run the **Sync TRM Product Names with Software Products** job, see [Run a job to sync TRM product names in EA Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-schedule-job-sync-trm-product-names.md).

</td></tr><tr><td>

**Update Score Range in Indicator Score Table**

</td><td>

Populates the TCO score range field on existing Indicator Score \[apm\_app\_indicator\_score\] records. Run this job on upgraded instances so the **Business applications by TCO score** widget on the **Portfolio TCO** dashboard displays TCO score bands instead of **\(empty\)**. The job is inactive by default and must be run on demand.

</td></tr></tbody>
</table>**Parent Topic:**[Enterprise Architecture Workspace reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-reference.md)

**Related topics**  


[Install Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/install-ea-workspace.md)

