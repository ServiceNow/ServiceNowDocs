---
title: Cancel an attestation schedule
description: Cancel an attestation schedule when you no longer want to create recurring asset attestations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/hardware-asset-management/cancel-attestation-schedule-ham.html
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Audit assets using Asset Attestation, Use, Hardware Asset Management, IT Asset Management]
---

# Cancel an attestation schedule

Cancel an attestation schedule when you no longer want to create recurring asset attestations.

## Before you begin

Role required: asset or inventory\_admin

## About this task

You can only cancel an asset attestation schedule that's in the Ready or In progress state. When you cancel the attestation schedule, the associated asset attestations that are in the In progress state aren't canceled. However, new asset attestations aren't created.

## Procedure

1.  Navigate to **Workspaces** &gt; **Hardware Asset Workspace** &gt; **Asset operations**.

2.  From the **Attestation** list, select **Schedules**.

    The list of all attestation schedules that are in the Ready, In progress, Closed complete, or Canceled state is displayed.

3.  Select an attestation schedule record that's in the Ready or In progress state.

4.  Select **Cancel schedule**.

5.  In the **Confirmation** dialog box, select **Yes**.


## Result

The state of the attestation schedule changes to Canceled.

**Parent Topic:**[Audit your hardware assets by using Asset Attestation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/audit-hardware-assets-attestation.md)

