---
title: Restart the Populate TPM Discovered Technologies and Lifecycles job
description: You can restart the Populate TPM Discovered Technologies and Lifecycles job if it encounters any interruptions or failures.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-portfolio-management/eaw-restart-tpm-scheduled-job.html
release: australia
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Working with Technology Lifecycle Management \(TLM\) in EA Workspace, Managing Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Restart the Populate TPM Discovered Technologies and Lifecycles job

You can restart the **Populate TPM Discovered Technologies and Lifecycles** job if it encounters any interruptions or failures.

## Before you begin

Role required: admin

## About this task

**Important:**

Technology Lifecycle Management \(TLM\) was previously known as Technology Portfolio Management \(TPM\). TPM and TLM refer to the same feature. Table names and scheduled job names continue to use TPM and haven't been renamed.

Whether your instance displays TPM or TLM also depends on your application versions. TLM labels appear only when both the Enterprise Architecture Workspace application \(version 9.2.1 or later\) and the Technology Lifecycle Management plugin, sn\_apm\_tpm \(version 1.11.0 or later\), are installed. If either application is on an earlier version, the interface continues to show TPM.

The restart feature enables you to resume the **Populate TPM Discovered Technologies and Lifecycles** job from where it stopped. This ensures that the data population process is completed without having to start the job from the beginning.

The **Restart** button is set to active on the Populate TPM Discovered Technology Run Log page after one hour with no update to the run log. You can determine whether the job faced any interruption or whether it failed by analyzing the **Records Processed** field value. If the count of TLM discovered technologies in the system stops increasing while the job is running, the job may have stalled or failed.

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Architecture Workspace**.

2.  Open the Setup page by selecting the Setup icon \[Omitted image "setup-icon.png"\] Alt text:.

3.  Select the expand row icon \(\[Omitted image "ExpandIcon.png"\] Alt text:\) next to **Logs**.

4.  Select the relevant TLM log for the **Populate TPM Discovered Technologies and Lifecycles** job you are restarting.

5.  Select **Restart**.


**Parent Topic:**[Working with Technology Lifecycle Management \(TLM\) in EA Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-portfolio-management/eaw-work-with-tpm.md)

**Related topics**  


[Exploring Technology Lifecycle Management \(TLM\) in Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-portfolio-management/eaw-tpm.md)

[Update TPM data for a business application or application service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-portfolio-management/update-tpm-data.md)

[View TPM logs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-portfolio-management/eaw-view-tpm-logs.md)

[Scheduled jobs for TLM in the EA Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-portfolio-management/eaw-tpm-scheduled-jobs.md)

