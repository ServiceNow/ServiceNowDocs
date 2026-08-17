---
title: Restart the TLM Discovered Technologies and Lifecycles job
description: You can restart the Restart TPM Discovered Technologies and Lifecycles job if it encounters any interruptions or failures.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-portfolio-management/eaw-restart-tpm-scheduled-job.html
release: zurich
topic_type: task
last_updated: "2026-07-17"
reading_time_minutes: 2
breadcrumb: [Working with Technology Lifecycle Management \(TLM\) in EA Workspace, Manage, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Restart the TLM Discovered Technologies and Lifecycles job

You can restart the **Restart TPM Discovered Technologies and Lifecycles** job if it encounters any interruptions or failures.

## Before you begin

Role required: admin

## About this task

**Important:**

Technology Lifecycle Management \(TLM\) was previously known as Technology Portfolio Management \(TPM\). TPM and TLM refer to the same feature. Table names and scheduled job names continue to use TPM and haven't been renamed.

Whether your instance displays TPM or TLM also depends on your application versions. TLM labels appear only when both the Enterprise Architecture Workspace application \(version 9.2.1 or later\) and the Technology Lifecycle Management plugin, sn\_apm\_tpm \(version 1.11.0 or later\), are installed. If either application is on an earlier version, the interface continues to show TPM.

The restart feature enables you to resume the **TPM Discovered Technologies and Lifecycles** job from where it stopped. This ensures that the data population process is completed without having to start the job from the beginning. The job discovers technologies from CMDB and Service Mapping relationships and then populates lifecycle records in the same run. Because both phases run as part of the same job, restarting it resumes both discovery and lifecycle population from the last processed record.

The **Restart** button is set to active on the **TLM Discovered Technology Run Log** page after one hour from the time since when there's no update to the run log. You can determine whether the job faced any interruption or whether it failed by analyzing the **Records Processed** field value. If the count of TLM discovered technologies in the system stops increasing while the job is running, the job may have stalled or failed.

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Architecture Workspace**.

2.  Open the Setup page by selecting the Setup icon \[Omitted image "setup-icon.png"\] Alt text: Setup icon.

3.  Select the expand row icon \(\[Omitted image "ExpandIcon.png"\] Alt text: Expand Row icon\) next to **Logs**.

4.  Select the relevant TLM log that you want to restart the **TPM Discovered Technologies and Lifecycles** job for.

5.  Select **Restart**.


**Parent Topic:**[Working with Technology Lifecycle Management \(TLM\) in EA Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-work-with-tpm.md)

**Related topics**  


[Manage the Technology Lifecycle Management \(TLM\) in Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-tpm.md)

[Update TLM data for a business application or application service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/update-tpm-data.md)

[View TLM logs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-view-tpm-logs.md)

