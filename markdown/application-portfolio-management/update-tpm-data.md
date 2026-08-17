---
title: Update TLM data for a business application or application service
description: Manually update the Technology Lifecycle Management \(TLM\) lifecycle data for software and hardware models in your business applications and application services.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/update-tpm-data.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Working with Technology Lifecycle Management \(TLM\) in EA Workspace, Managing Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Update TLM data for a business application or application service

Manually update the Technology Lifecycle Management \(TLM\) lifecycle data for software and hardware models in your business applications and application services.

## Before you begin

Role required: sn\_apm.apm\_user

## About this task

**Important:**

Technology Lifecycle Management \(TLM\) was previously known as Technology Portfolio Management \(TPM\). TPM and TLM refer to the same feature. Table names and scheduled job names continue to use TPM and haven't been renamed.

Whether your instance displays TPM or TLM also depends on your application versions. TLM labels appear only when both the Enterprise Architecture Workspace application \(version 9.2.1 or later\) and the Technology Lifecycle Management plugin, sn\_apm\_tpm \(version 1.11.0 or later\), are installed. If either application is on an earlier version, the interface continues to show TPM.

You can refresh the TLM lifecycle data manually for a selected business application or application service. A scheduled job **Populate TPM Discovered Technologies and Lifecycles** is also run on schedule or on-demand to update the lifecycle data for all business applications and application services​​.

**Note:** The data for software products is displayed only when the Software Asset Management \(SAM\) Foundation or Software Asset Management \(SAM\) Professional plugin is installed.

TLM lifecycle record identifiers are automatically generated on creating a TLM record using the Technology Lifecycle Management \(sn\_apm\_tpm\) plugin version 1.9.0. However, for TLM lifecycle records generated using previous versions of the TLM plugin don't have any lifecycle record identifiers. The TLM record identifiers of these TLM lifecycle records must be generated using the Populate Number field in **TPM Discovered Technologies** job. For information, see [Run a scheduled job to populate Technology Lifecycle Management lifecycle record identifier](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-run-job-to-populate-tpm-lifecycle-identifier.md).

\[Omitted image "tpm-lifecycle-record.png"\] Alt text: TLM lifecycle record identifier highlighted on the Technology Portfolio page.

On selecting a TLM lifecycle record identifier, more information on the TLM lifecycle record is displayed.

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Architecture Workspace**.

2.  Open the Portfolio List view by selecting the portfolio icon \(\[Omitted image "icon-portfolio.png"\] Alt text: Portfolio view\).

3.  Expand Application Portfolio and select **Business Applications**.

4.  Select the relevant business application.

5.  Select the three-dot menu \(\[Omitted image "icon-three-dot-menu.png"\] Alt text: Three-dot menu\) and select **Update TPM Data**.


## Result

An on-demand job starts to update the TLM data.

**Parent Topic:**[Working with Technology Lifecycle Management \(TLM\) in EA Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-work-with-tpm.md)

**Related topics**  


[Restart the TLM Discovered Technologies and Lifecycles job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-restart-tpm-scheduled-job.md)

