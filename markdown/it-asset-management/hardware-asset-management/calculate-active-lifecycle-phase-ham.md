---
title: Calculate the active lifecycle phase for a model
description: Recalculate the active life cycle phase for a hardware or consumable model without waiting for the scheduled daily job.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-asset-management/hardware-asset-management/calculate-active-lifecycle-phase-ham.html
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-10-06"
reading_time_minutes: 6
keywords: [Active lifecyle phase, Refresh lifecyle phase, Hardware model, Consumable model]
breadcrumb: [Use, Hardware Asset Management, IT Asset Management, Asset Management]
---

# Calculate the active lifecycle phase for a model

Recalculate the active life cycle phase for a hardware or consumable model without waiting for the scheduled daily job.

## Before you begin

Role required: model\_manager or asset

## About this task

After you normalize hardware and consumable models, the lifecycle phases on the model lifecycle records are marked as inactive, including the current phase that is active. The system corrects this status only after the HAM - Hardware Normalization scheduled job runs, which can take up to 24 hours. Use the **Calculate Lifecycle Phase** option to refresh the lifecycle phase status immediately.

## Procedure

1.  Navigate to **Workspaces** &gt; **Hardware Asset Workspace** &gt; **Model management**.

2.  Select the model tab.

    -   Select **Hardware models** for hardware model records
    -   Select **Consumable models** for consumable model records
3.  Select the model record.

4.  Select the appropriate lifecycle tab.

    -   **Hardware Model Lifecycles** tab for hardware model records
    -   **Consumable Model Lifecycles** tab for hardware model records
5.  Select **Calculate Lifecycle Phase**.


## Result

The system recalculates and identifies the correct active lifecycle phase, updating the current\_lifecycle\_phase flag to true for that phase while marking all other phases as inactive.

**Parent Topic:**[Using Hardware Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/hardware-asset-management/using-ham-classic.md)

**Related topics**  


[Analyze hardware assets using the Generate hardware asset insights generative AI skill]()

[Work with hardware normalization]()

[Manage asset bundles from your inventory]()

[Manage your inventory through pallet assets]()

[Manage loaner assets]()

[Donate assets to charity organizations]()

[Use Advanced Shipment Notification]()

[Manage RMA requests]()

[Create an inventory stock order request]()

[Create a disposal order]()

[Fulfilling hardware asset requests]()

[Audit hardware asset inventory]()

[Request a Hardware Asset Refresh]()

[Manage your expiring contracts for leased hardware assets]()

[Reclaim hardware assets]()

[View RFID information of assets]()

[Manage the lifecycle of hardware models with calculated lifecycle templates]()

[Create an internal lifecycle in the Hardware Asset Workspace]()

[Receive asset warranty details from Lenovo]()

[Manage stockrooms]()

[Track shipments using the integration framework]()

[Track asset location using indoor maps]()

[Assess performance of Hardware Asset Management]()

[Manage refresh of assets using Zero Touch Refresh]()

[Configure the Total Cost of Ownership of assets]()

[Manage Hardware Asset Management subscriptions]()

[Manage repair of defective assets in your stockroom in the Hardware Asset Workspace]()

[Manage picking hardware assets within your stockroom for Hardware Asset Management workflows]()

[Manage hardware asset tasks using the Mobile Agent application]()

[Manage asset put away using the Hardware Asset Workspace]()

[Audit your hardware assets by using Asset Attestation]()

[Manage contract repository agentic workflow in the Hardware Asset Workspace]()

[Manage obligations in the Hardware Asset Workspace]()

[Acknowledge receipt of assets on the Employee Center portal]()

[Update associated Decision tables for HAM flows]()

