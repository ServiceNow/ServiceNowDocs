---
title: Repair flow to fix defective enterprise assets within a stockroom
description: Use the repair flow to get the defective enterprise assets in your stockroom fixed so that the repaired assets can be used in different Enterprise Asset Management workflows.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Exploring Enterprise Asset Management, Enterprise Asset Management, IT Asset Management]
---

# Repair flow to fix defective enterprise assets within a stockroom

Use the repair flow to get the defective enterprise assets in your stockroom fixed so that the repaired assets can be used in different Enterprise Asset Management workflows.

By using the Repair flow, your organization can internally fix the assets that are damaged or out of the warranty period. The repaired assets can be put back to use after validation. There's no external vendor involved in the repair of defective assets.

As an asset manager, you can request repair of assets that are either defective or pending repair in your stockroom by submitting repair orders. For more details, see [Request repair of defective enterprise assets](request-repair-defective-eam-assets.md). The repair flow is triggered when you submit a repair order. A repair order has repair order lines that are associated with repair tasks for the assets. The asset technician completes the repair tasks associated with the repair order. The repair flow completes after the repaired asset is evaluated. For more details, see [Manage repair of defective assets in your stockroom in the Enterprise Asset Workspace](manage-repair-of-defective-eam-assets.md) and [Manage enterprise asset repair tasks using the Mobile Agent application](repair-orders-mobile-agent-eam.md).

## Stages in the Repair flow

1.  Troubleshoot: Stage to evaluate the defective asset and assess the following:

    -   Issues with the asset
    -   Parts required
    -   Steps to repair the defective asset
    At this stage, an asset technician confirms if the asset is repairable, redeployable, or unrepairable. The Repair flow proceeds to the next stage only if the asset is repairable. Otherwise the repair order is marked as Complete.

2.  Repair: Stage to confirm repair of the defective asset. In this task, the asset is either repaired, redeployed, or marked as unrepairable.

    The repair flow proceeds to the next stage only if the asset is repaired. Otherwise the repair order is marked as Complete.

3.  Evaluate: Stage to perform a quality control check of the repaired asset. Based on the evaluation results, the asset is either redeployed or disposed of. The Repair flow is completed after asset evaluation.

**Note:** You can specify the reason for the asset failure using failure codes in the Troubleshoot asset and Repair asset tasks. You can also specify the solution that you applied to address the asset issue using the resolution codes in the Repair asset task. These details are also available on the repair order line form. For more details, see [Failure and resolution codes in Enterprise Asset Management](failure-resolution-codes-eam.md).

The failure and resolution codes are available with Enterprise Asset Management version 9.0 and later.

