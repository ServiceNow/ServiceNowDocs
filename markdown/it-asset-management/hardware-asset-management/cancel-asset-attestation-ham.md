---
title: Cancel an asset attestation
description: Cancel an asset attestation when you no longer have to validate the ownership of the serialized assets.
locale: en-US
release: yokohama
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Audit your hardware assets by using Asset Attestation, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Cancel an asset attestation

Cancel an asset attestation when you no longer have to validate the ownership of the serialized assets.

## Before you begin

Role required: asset or inventory\_admin

## About this task

An asset attestation that's in the In progress state can only be canceled.

## Procedure

1.  Navigate to **Workspaces** &gt; **Hardware Asset Workspace** &gt; **Asset operations**.

2.  From the **Attestation** list, select **Attestations**.

    The list of all asset attestations that are in the In progress, Closed complete, or Canceled state is displayed.

3.  Select an attestation record that's in the In progress state.

4.  Select **Cancel attestation**.

5.  In the Confirmation dialog box, select **Yes**.


## Result

-   The state of the asset attestation changes to Canceled.
-   The status of the assets in the asset attestation that aren't confirmed by the employees' changes from Open to Canceled.

**Parent Topic:**[Audit your hardware assets by using Asset Attestation](../concept/audit-hardware-assets-attestation.md)

