---
title: Update verification status of TLM audit details
description: Change the verification status of a software product or hardware model lifecycle in the TLM technology lifecycle exception table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-update-verif-status.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [View technology portfolio audit risk details, Working with Technology Lifecycle Management \(TLM\) in EA Workspace, Managing Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Update verification status of TLM audit details

Change the verification status of a software product or hardware model lifecycle in the TLM technology lifecycle exception table.

## Before you begin

Role required: sn\_apm.apm\_analyst

## About this task

**Important:**

Technology Lifecycle Management \(TLM\) was previously known as Technology Portfolio Management \(TPM\). TPM and TLM refer to the same feature. Table names and scheduled job names continue to use TPM and haven't been renamed.

Whether your instance displays TPM or TLM also depends on your application versions. TLM labels appear only when both the Enterprise Architecture Workspace application \(version 9.2.1 or later\) and the Technology Lifecycle Management plugin, sn\_apm\_tpm \(version 1.11.0 or later\), are installed. If either application is on an earlier version, the interface continues to show TPM.

You can acknowledge a heuristic lifecycle match of a product by changing its status to verified or rejected.

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Architecture Workspace**.

2.  Open the Technology Portfolio page by selecting the Technology Portfolio icon \[Omitted image "technology-portfolio-icon.png"\] Alt text: Technology portfolio icon.

3.  Select **Technology Portfolio Audit** tab.

4.  Open a product type \(Software or Hardware\) by selecting it.

5.  In the TLM Technology Lifecycle Exception form, set the **Verification Status** to either **Verified** or **Rejected**.

    If the lifecycle phase is set to **Verified**, then the exception count is reduced in the Technology Lifecycle table. If the lifecycle phase is set to **Rejected**, then the exception count is reduced and dates for that lifecycle phase will not appear in the Technology Lifecycle table.

6.  Add comments in the **Comments** box.

7.  Select **Save**.


**Parent Topic:**[View technology portfolio audit risk details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-view-audit-risk-details.md)

**Related topics**  


[View technology portfolio audit risk details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-view-audit-risk-details.md)

