---
title: Update TPM data for a business application or application service
description: Manually update the Technology Portfolio Management \(TPM\) lifecycle data including end of support date, end of extended support date, and end of life date for your software and hardware models for your business applications and application services.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Managing the Technology Portfolio Management \(TPM\) in Enterprise Architecture Workspace, Technology Portfolio view, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Update TPM data for a business application or application service

Manually update the Technology Portfolio Management \(TPM\) lifecycle data including end of support date, end of extended support date, and end of life date for your software and hardware models for your business applications and application services.

## Before you begin

Role required: admin

## About this task

You can refresh the TPM lifecycle data manually for a selected business application or application service. A scheduled job **Populate TPM Discovered Technologies and Lifecycles** is also run on schedule or on-demand to update the lifecycle data for all business applications and application services​​.

**Note:** The data for software products is displayed only when the Software Asset Management \(SAM\) Foundation or Software Asset Management \(SAM\) Professional plugin is installed.

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Architecture Workspace**.

2.  Open the Portfolio List view by selecting the portfolio icon \(![Portfolio view](../image/icon-portfolio.png)\).

3.  Expand Application Portfolio and select **Business Applications**.

4.  Select the relevant business application.

5.  Select the three-dot menu \(![Three-dot menu](../image/icon-three-dot-menu.png)\) and select **Update TPM Data**.


## Result

An on-demand job starts to update the TPM data.

**Parent Topic:**[Managing the Technology Portfolio Management \(TPM\) in Enterprise Architecture Workspace](../concept/eaw-concept/eaw-tpm.md)

**Related topics**  


[Schedule a job to generate TPM lifecycle data](schedule-job-generate-tpm-data.md)

[Run a scheduled job to generate TPM lifecycle data](run-scheduled-job-update-tpm-data.md)

