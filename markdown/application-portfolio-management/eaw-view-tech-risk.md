---
title: View TPM risk details
description: View all the Technology Portfolio Management \(TPM\) risk data for software products that are facing high and moderate technology risks.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Working with Technology Portfolio Management \(TPM\) in EA Workspace, Managing Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# View TPM risk details

View all the Technology Portfolio Management \(TPM\) risk data for software products that are facing high and moderate technology risks.

## Before you begin

Role required: sn\_apm.apm\_user

## About this task

You can use the TPM risk scores to manage and mitigate the risks associated with your software products and hardware models.

The TPM risk details of software products and hardware models are calculated based on their lifecycle dates that are the end of support, end of extended support, and end of life dates. The sum of the related software and hardware risk score is the risk score of an application service. And the sum of the related application service risk score is considered as the risk score of a business application.

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Architecture Workspace**.

2.  Open the Technology Portfolio page by selecting the Technology Portfolio icon ![Technology portfolio icon](../../image/eaw-image/technology-portfolio-icon.png).

3.  Select **TPM risk**.

    To update the TPM risk scores, you must run the **Populate Technology Lifecycles Risks** job. For more details, see [Schedule a job to generate TPM technology risk](eaw-schedule-job-generate-tpm-risk.md).


**Parent Topic:**[Working with Technology Portfolio Management \(TPM\) in EA Workspace](../../concept/eaw-concept/eaw-work-with-tpm.md)

**Related topics**  


[Update TPM data for a business application or application service](update-tpm-data.md)

[Restart Populate TPM Discovered Technologies and Lifecycles scheduled job](eaw-restart-tpm-scheduled-job.md)

[Update the system property to gather software products from a CMDB table](eaw-update-system-property-gather-software-cmdb.md)

[View technology portfolio audit risk details](eaw-view-audit-risk-details.md)

[Update verification status of TPM audit details](../eaw-update-verif-status.md)

[View TPM logs](eaw-view-tpm-logs.md)

