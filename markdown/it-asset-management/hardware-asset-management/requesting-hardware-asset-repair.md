---
title: Repair flow to fix defective hardware assets within a stockroom
description: Use the Repair flow to get the defective hardware assets in your stockroom fixed so that the repaired assets can be used in different Hardware Asset Management workflows.
locale: en-US
release: xanadu
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Exploring Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Repair flow to fix defective hardware assets within a stockroom

Use the Repair flow to get the defective hardware assets in your stockroom fixed so that the repaired assets can be used in different Hardware Asset Management workflows.

By using the Repair flow, your organization can internally fix the assets that are damaged or out of the warranty period. The repaired assets can be put back to use after validation. There's no external vendor involved in the repair of defective assets.

As an asset manager, you can request repair of assets that are either defective or pending repair in your stockroom by submitting repair orders. For more details, see [Request repair of defective hardware assets in your stockroom](request-repair-defective-ham-assets.md). The repair flow is triggered when you submit a repair order. A repair order has repair order lines that are associated with repair tasks for the assets. The asset technician completes the repair tasks in the Hardware Asset Workspace or by using the Mobile Agent application. The repair flow completes after the repaired asset is evaluated. For details, see [Manage repair of defective assets in your stockroom in the Hardware Asset Workspace](manage-repair-of-defective-ham-assets.md) and [Manage hardware asset repair tasks using the Mobile Agent application](repair-orders-mobile-agent-ham.md).

## Stages in the Repair flow

1.  Troubleshoot: Stage to evaluate the defective asset and assess the following:

    -   Issues with the asset
    -   Parts required
    -   Steps to repair the defective asset
    At this stage, an asset technician confirms if the asset is repairable, redeployable, or unrepairable. The Repair flow proceeds to the next stage only if the asset is repairable. Otherwise the repair order is marked as Complete.

2.  Repair: Stage to confirm repair of the defective asset. In this task, the asset is either repaired, redeployed, or marked as unrepairable.

    The repair flow proceeds to the next stage only if the asset is repaired. Otherwise the repair order is marked as Complete.

3.  Evaluate: Stage to perform a quality control check of the repaired asset. Based on the evaluation results, the asset is either redeployed or disposed of. The Repair flow is completed after asset evaluation.

