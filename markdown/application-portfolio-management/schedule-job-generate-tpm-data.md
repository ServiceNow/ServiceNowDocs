---
title: Schedule a job to generate TPM lifecycle data
description: Enable the  Populate TPM Discovered Technologies and Lifecycles scheduled job to regularly compute the technology lifecycle risks.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Schedule a job to generate TPM lifecycle data

Enable the  **Populate TPM Discovered Technologies and Lifecycles** scheduled job to regularly compute the technology lifecycle risks.

## Before you begin

Role required: admin

**Note:** The data for software products is displayed only when the Software Asset Management \(SAM\) Foundation or Software Asset Management \(SAM\) Professional plugin is installed.

## Procedure

1.  Navigate to **All** &gt; **System Scheduler ** &gt; ** Scheduled Jobs** &gt; ** Scheduled Jobs**.

2.  Find and select the  **Populate TPM Discovered Technologies and Lifecycles** scheduled job.

3.  In the **Next action** field, select a date and time to run the job.

4.  Click  **Update**.


## Result

The job will run as scheduled to generate the TPM lifecycle data.

**Note:** You can also run the job on-demand. For details, see [Run a scheduled job to generate TPM lifecycle data](run-scheduled-job-update-tpm-data.md).

**Parent Topic:**[Configuring Enterprise Architecture \(formerly Application Portfolio Management\)](../concept/configure-apm.md)

