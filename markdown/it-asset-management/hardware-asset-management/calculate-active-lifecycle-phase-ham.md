---
title: Calculate the active lifecycle phase for a model
description: Recalculate the active life cycle phase for a hardware or consumable model without waiting for the scheduled daily job.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/hardware-asset-management/calculate-active-lifecycle-phase-ham.html
release: brazil
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-10-06"
reading_time_minutes: 2
keywords: [Active lifecyle phase, Refresh lifecyle phase, Hardware model, Consumable model]
breadcrumb: [Asset lifecycle and disposal, Use, Hardware Asset Management, IT Asset Management, Asset Management]
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

**Parent Topic:**[Asset lifecycle and disposal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/asset-lifecycle-disposal-ham.md)

**Related topics**  


[Request a Hardware Asset Refresh]()

[Manage refresh of assets using Zero Touch Refresh]()

[Manage your expiring contracts for leased hardware assets]()

[Reclaim hardware assets]()

[Create a disposal order]()

[Donate assets to charity organizations]()

[Manage asset bundles from your inventory]()

[Manage obligations in the Hardware Asset Workspace]()

[Manage contract repository agentic workflow in the Hardware Asset Workspace]()

