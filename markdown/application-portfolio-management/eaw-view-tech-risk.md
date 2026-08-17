---
title: View TLM risk details
description: View all the Technology Lifecycle Management \(TLM\) risk data for software products that are facing high and moderate technology risks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-view-tech-risk.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Working with Technology Lifecycle Management \(TLM\) in EA Workspace, Managing Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# View TLM risk details

View all the Technology Lifecycle Management \(TLM\) risk data for software products that are facing high and moderate technology risks.

## Before you begin

Role required: sn\_apm.apm\_user

## About this task

**Important:**

Technology Lifecycle Management \(TLM\) was previously known as Technology Portfolio Management \(TPM\). TPM and TLM refer to the same feature. Table names and scheduled job names continue to use TPM and haven't been renamed.

Whether your instance displays TPM or TLM also depends on your application versions. TLM labels appear only when both the Enterprise Architecture Workspace application \(version 9.2.1 or later\) and the Technology Lifecycle Management plugin, sn\_apm\_tpm \(version 1.11.0 or later\), are installed. If either application is on an earlier version, the interface continues to show TPM.

You can use the TLM risk scores to manage and mitigate the risks associated with your software products and hardware models.

The TLM risk details of software products and hardware models are calculated based on their lifecycle dates. These dates include end of support, end of extended support, and end of life. The sum of the related software and hardware risk score is the risk score of an application service. The sum of the related application service risk score is the risk score of a business application.

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Architecture Workspace**.

2.  Open the Technology Portfolio page by selecting the Technology Portfolio icon \[Omitted image "technology-portfolio-icon.png"\] Alt text: Technology portfolio icon.

3.  Select **TLM risk**.

    To update the TLM risk scores, you must run the **Populate Technology Lifecycles Risks** job. For more details, see [Schedule a job to generate TLM technology risk](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-schedule-job-generate-tpm-risk.md).


**Parent Topic:**[Working with Technology Lifecycle Management \(TLM\) in EA Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-work-with-tpm.md)

**Related topics**  


[Update TLM data for a business application or application service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/update-tpm-data.md)

[Restart the TLM Discovered Technologies and Lifecycles job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-restart-tpm-scheduled-job.md)

[Update the system property to gather software products from a CMDB table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-update-system-property-gather-software-cmdb.md)

[View technology portfolio audit risk details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-view-audit-risk-details.md)

[Update verification status of TLM audit details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-update-verif-status.md)

[View TLM logs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-view-tpm-logs.md)

