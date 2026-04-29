---
title: Manage repair of defective assets in your stockroom in the Enterprise Asset Workspace
description: Use the Repair flow to get the defective enterprise assets in your stockroom fixed so that the repaired assets can be used in different Enterprise Asset Management workflows.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create and manage enterprise asset inventory, Managing enterprise asset inventory and contracts, Enterprise Asset Management, IT Asset Management]
---

# Manage repair of defective assets in your stockroom in the Enterprise Asset Workspace

Use the Repair flow to get the defective enterprise assets in your stockroom fixed so that the repaired assets can be used in different Enterprise Asset Management workflows.

By using the Repair flow, your organization can internally fix the assets that are damaged or out of the warranty period. The repaired assets can be put back to use after validation. There's no external vendor involved in the repair of defective assets.

As an asset manager, you can request repair of assets that are either defective or pending repair in your stockroom by submitting repair orders. For more details, see [Request repair of defective enterprise assets](request-repair-defective-eam-assets.md). The repair flow is triggered when you submit a repair order. A repair order has repair order lines that are associated with repair tasks for the assets. The asset technician completes the repair tasks associated with the repair order. The repair flow completes after the repaired asset is evaluated and either put to use or disposed of.

**Note:** Asset technician can also complete the repair tasks by using the Mobile Agent application.

## Stages in the Repair flow

1.  Troubleshoot: Stage to evaluate the defective asset and assess the following:

    -   Issues with the asset
    -   Parts required
    -   Steps to repair the defective asset
    At this stage, an asset technician confirms if the asset is repairable, redeployable, or unrepairable. The Repair flow proceeds to the next stage only if the asset is repairable. Otherwise the repair order is marked as Complete.

2.  Repair: Stage to confirm repair of the defective asset. In this task, the asset is either repaired, redeployed, or marked as unrepairable.

    The repair flow proceeds to the next stage only if the asset is repaired. Otherwise the repair order is marked as Complete.

3.  Evaluate: Stage to perform a quality control check of the repaired asset. Based on the evaluation results, the asset is either redeployed or disposed of. The Repair flow is completed after asset evaluation.

**Note:** You can specify the reason for the asset failure using failure codes in the Troubleshoot asset and Repair asset tasks. You can also specify the solution that you applied to address the asset issue using the resolution codes in the Repair asset task. These details are also available on the repair order line form. For more details, see [Manage failure and resolution codes](manage-failure-res-codes-eam.md).

-   **[Request repair of defective enterprise assets](request-repair-defective-eam-assets.md)**  
As an enterprise asset manager, you can get the defective enterprise assets repaired by creating Repair orders.
-   **[Fulfilling repair orders in the Enterprise Asset Workspace](fulfilling-repair-orders-eam.md)**  
You can fulfill repair orders for your defective and out-of-warranty enterprise assets by completing all repair asset tasks that are associated with the corresponding repair order lines. You can fulfill these orders either manually or through the help repair enterprise assets agentic workflow.
-   **[Record time worked on asset repair tasks in the Enterprise Asset Workspace](record-repair-time-eam-ws.md)**  
Manage and record time worked on Troubleshoot asset, Repair asset, and Evaluate asset tasks in the Enterprise Asset Workspace. After you start work on a repair asset task, you can pause and resume work. You can also record the time worked manually.

**Parent Topic:**[Create and manage enterprise asset inventory](managing-enterprise-asset-inventory.md)

