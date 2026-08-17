---
title: Run a scheduled job to generate TLM lifecycle data
description: Run a scheduled job to fetch the technology lifecycle data for your technology portfolio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-run-scheduled-job-update-tpm-data.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Working with Technology Lifecycle Management \(TLM\) in EA Workspace, Managing Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Run a scheduled job to generate TLM lifecycle data

Run a scheduled job to fetch the technology lifecycle data for your technology portfolio.

## Before you begin

Role required: admin

## About this task

**Important:**

Technology Lifecycle Management \(TLM\) was previously known as Technology Portfolio Management \(TPM\). TPM and TLM refer to the same feature. Table names and scheduled job names continue to use TPM and haven't been renamed.

Whether your instance displays TPM or TLM also depends on your application versions. TLM labels appear only when both the Enterprise Architecture Workspace application \(version 9.2.1 or later\) and the Technology Lifecycle Management plugin, sn\_apm\_tpm \(version 1.11.0 or later\), are installed. If either application is on an earlier version, the interface continues to show TPM.

The scheduled job **Populate TPM Discovered Technologies and Lifecycles** is created to fetch the technology lifecycle data for your technology portfolio. This job can be run on-demand to calculate the technology lifecycle risk. The scheduled job executes the script generating the lifecycle risk dates for your software and hardware models. These dates include end of support date, end of extended support date, and end of life date.

**Note:** The data for software products is displayed only the Software Asset Management \(SAM\) Foundation or Software Asset Management \(SAM\) Professional plugin is installed.

## Procedure

1.  Navigate to **All** &gt; ** System Definition ** &gt; ** Scheduled Jobs**.

2.  Find and open the  scheduled job **Populate TPM Discovered Technologies and Lifecycles**.

3.  Select  ** Execute Now**.


## Result

After executing the scheduled job, the engine automatically stores the technologies and lifecycle values in the TPM Technology Lifecycle \[sn\_apm\_tpm\_technology\_lifecycle\] table. It updates the values in the table each time after you run the job.

## What to do next

To know the status of the scheduled job, refer to the TPM Discovered Technology Run Logs \[sn\_apm\_tpm\_discovered\_technology\_run\_log\] table. To view the technology lifecycle information, refer to the TPM Technology Lifecycle \[sn\_apm\_tpm\_technology\_lifecycle\] table. You can view the results in the **Enterprise Architecture Workspace** &gt; **Settings** &gt; **Logs** &gt; **TLM Logs**.

**Parent Topic:**[Working with Technology Lifecycle Management \(TLM\) in EA Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-work-with-tpm.md)

