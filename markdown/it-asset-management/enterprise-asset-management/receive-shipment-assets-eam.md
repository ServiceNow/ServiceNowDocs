---
title: Receive assets from inbound shipments at your stockroom in the Enterprise Asset Workspace
description: Receive enterprise and consumable assets from one or more shipments that are in transit to your stockroom in the Enterprise Asset Workspace. You can receive assets from shipments originating from any workflow.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Manage the receiving of assets at stockrooms in the Enterprise Asset Workspace, Create and manage enterprise asset inventory, Manage enterprise asset inventory and contracts, Enterprise Asset Management, IT Asset Management]
---

# Receive assets from inbound shipments at your stockroom in the Enterprise Asset Workspace

Receive enterprise and consumable assets from one or more shipments that are in transit to your stockroom in the Enterprise Asset Workspace. You can receive assets from shipments originating from any workflow.

## Before you begin

Role required: sn\_eam.asset\_technician or sn\_eam.enterprise\_asset\_manager

## About this task

If you don't have the details of the assets you want to receive at your stockroom, you can view the list of assets that are on their way and then receive them. You can receive the complete quantity of consumables in the shipments, not a partial quantity.

Assets from an inbound shipment can be received under the following conditions:

-   The assets must have a serial number and an asset tag.
-   The assets must be in the In-transit state and linked to a shipment record.
-   Hardware assets can be received only if the Hardware Asset Management application is activated.

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Asset Workspace** &gt; **Inventory**.

2.  Select the **All stockrooms** tab.

3.  Select the stockroom for which you want to receive hardware or consumable assets.

4.  Select **Receive assets**.

5.  In the Receive assets dialog box, select **View all inbound assets**.

    A list of all shipment assets currently on their way to the stockroom is displayed.

    The following details of a shipment are displayed:

    -   **Asset**: Display name of the asset.
    -   **Stage**: Stage of the shipment.

        **Note:** Only shipments that are In transit are displayed.

    -   **Model categories**: Model grouping of the asset.
    -   **Quantity**: Number of assets to be received.
    -   **Asset tag**: Tag to track the asset.
    -   **Serial number**: Serial number of the asset.
    -   **Tracking number**: Identifier to track the shipment.
    -   **Source**: Details of the source workflow including the request number through which you’re receiving the asset. The source could be a transfer order line, a purchase order line, an RMA order line, or any other workflow through which the asset is received.
6.  Select the shipment asset that you want to receive and then select **Receive**.


## Result

If the asset details are valid, the following changes occur:

-   The assets are received successfully.
-   The State of the assets changes from **In transit** to **In stock**, and the Substate of the assets changes from **Reserved** to **Available**.
-   The stockroom field on the asset form is automatically updated with the stockroom at which you received the assets.
-   The Status of the shipment tasks associated with the assets changes to **Delivered**.
-   The receive tasks in the source workflows are automatically closed.

If any of the asset details are invalid, an error message in shown in the **Alert** column for the corresponding asset record. You should resolve the error before receiving the assets.

**Parent Topic:**[Manage the receiving of assets at stockrooms in the Enterprise Asset Workspace](../concept/manage-stockroom-receive-eam.md)

