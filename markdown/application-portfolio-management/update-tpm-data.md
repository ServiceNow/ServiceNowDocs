---
title: Update TPM data for a business application or application service
description: Manually update the Technology Portfolio Management \(TPM\) lifecycle data including end of support date, end of extended support date, and end of life date for your software and hardware models for your business applications and application services.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/update-tpm-data.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Working with Technology Portfolio Management \(TPM\) in EA Workspace, Managing Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Update TPM data for a business application or application service

Manually update the Technology Portfolio Management \(TPM\) lifecycle data including end of support date, end of extended support date, and end of life date for your software and hardware models for your business applications and application services.

## Before you begin

Role required: sn\_apm.apm\_user

## About this task

You can refresh the TPM lifecycle data manually for a selected business application or application service. A scheduled job **Populate TPM Discovered Technologies and Lifecycles** is also run on schedule or on-demand to update the lifecycle data for all business applications and application services​​.

**Note:** The data for software products is displayed only when the Software Asset Management \(SAM\) Foundation or Software Asset Management \(SAM\) Professional plugin is installed.

TPM lifecycle record identifiers are automatically generated on creating a TPM record using the Technology Portfolio Management \(sn\_apm\_tpm\) plugin version 1.9.0. However, for TPM lifecycle records generated using previous versions of the TPM plugin don't have any lifecycle record identifiers. The TPM record identifiers of these TPM lifecycle records must be generated using the Populate Number field in TPM Discovered Technologies job. For information, see [Run a scheduled job to populate Technology Portfolio Management lifecycle record identifier](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-run-job-to-populate-tpm-lifecycle-identifier.md).

\[Omitted image "tpm-lifecycle-record.png"\] Alt text: TPM lifecycle record identifier highlighted on the Technology Portfolio page.

On selecting a TPM lifecycle record identifier, more information on the TPM lifecycle record is displayed.

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Architecture Workspace**.

2.  Open the Portfolio List view by selecting the portfolio icon \(\[Omitted image "icon-portfolio.png"\] Alt text: Portfolio view\).

3.  Expand Application Portfolio and select **Business Applications**.

4.  Select the relevant business application.

5.  Select the three-dot menu \(\[Omitted image "icon-three-dot-menu.png"\] Alt text: Three-dot menu\) and select **Update TPM Data**.


## Result

An on-demand job starts to update the TPM data.

**Parent Topic:**[Working with Technology Portfolio Management \(TPM\) in EA Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-work-with-tpm.md)

**Related topics**  


[Restart Populate TPM Discovered Technologies and Lifecycles scheduled job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-restart-tpm-scheduled-job.md)

