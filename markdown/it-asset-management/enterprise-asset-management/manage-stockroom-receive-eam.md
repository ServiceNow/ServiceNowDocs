---
title: Manage the receiving of assets at stockrooms in the Enterprise Asset Workspace
description: As an enterprise asset manager or enterprise asset technician, receive enterprise and consumable assets at stockrooms from any workflow at a centralized location on the stockroom form in the Enterprise Asset Workspace.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Create and manage enterprise asset inventory, Managing enterprise asset inventory and contracts, Enterprise Asset Management, IT Asset Management]
---

# Manage the receiving of assets at stockrooms in the Enterprise Asset Workspace

As an enterprise asset manager or enterprise asset technician, receive enterprise and consumable assets at stockrooms from any workflow at a centralized location on the stockroom form in the Enterprise Asset Workspace.

With the standardized receiving process, you don't need to be familiar with the specific workflow to which the assets belong. Therefore, you can receive hardware and consumable assets from different shipments originating from sources, like transfer orders, purchase orders, or any other workflows seamlessly.

## Requirements and limitations

-   You can receive enterprise assets in the Hardware Asset Workspace only if the Enterprise Asset Management application is activated.
-   You can receive hardware assets in the Enterprise Asset Workspace only if the Hardware Asset Management application is activated.
-   You can only receive complete quantity of consumables.
-   You can receive assets from a purchase order line only in the Zurich or later releases.

## Asset receiving mechanisms

You can receive a single asset or multiple assets in bulk using any of the following options on the enhanced stockroom form:

-   **Receive assets**: You can either search for an asset using its Asset Tag, Serial Number, or MAC address and receive it, or select one or more assets from the list of inbound shipment assets and receive them. For more details, see [Receive an enterprise asset at a stockroom in the Enterprise Asset Workspace](../task/receive-assets-stockroom-eam.md) and [Receive assets from inbound shipments at your stockroom in the Enterprise Asset Workspace](../task/receive-shipment-assets-eam.md).
-   **Import assets**: You can download the Excel template, add the asset details that you want to receive, and import the Excel template. During the import process, the system performs validations, and you can view the imported asset records, validation status, and comments in the Import asset row \[sn\_itam\_cmn\_import\_asset\_row\] table. Based on the validation status, you can select and receive the assets. If there are any issues with the asset records, you must address those issues before you can receive the assets. For more details, see [Import and receive assets in bulk at your stockroom in the Enterprise Asset Workspace](../task/import-assets-for-receive-eam.md).

When any asset is received at the stockroom, the following changes happen:

-   The State of the asset changes from **In transit** to **In stock**.
-   The stockroom field on the asset form is automatically updated.
-   The receive tasks in the source workflows associated with the asset that you received are automatically closed.

Depending on the number and type of assets that you want to receive, you can select from the following options to receive assets at your stockroom:

-   [Receive a single enterprise asset at your stockroom](../task/receive-assets-stockroom-eam.md).
-   [Receive one or more enterprise and consumable assets from the list of shipment assets](../task/receive-shipment-assets-eam.md).
-   [Import and receive enterprise and consumable assets in bulk through an Excel template](../task/import-assets-for-receive-eam.md).

    **Note:** You should have the sn\_eam.enterprise\_admin role to import asset records using the Excel template.


-   **[Receive an enterprise asset at a stockroom in the Enterprise Asset Workspace](../task/receive-assets-stockroom-eam.md)**  
Receive a single enterprise asset that has arrived at your stockroom, whether it's part of a workflow or not, in the Enterprise Asset Workspace.
-   **[Receive assets from inbound shipments at your stockroom in the Enterprise Asset Workspace](../task/receive-shipment-assets-eam.md)**  
Receive enterprise and consumable assets from one or more shipments that are in transit to your stockroom in the Enterprise Asset Workspace. You can receive assets from shipments originating from any workflow.
-   **[Import and receive assets in bulk at your stockroom in the Enterprise Asset Workspace](../task/import-assets-for-receive-eam.md)**  
Receive multiple enterprise and consumable assets at your stockroom by importing the asset records using an Excel template in the Enterprise Asset Workspace.

**Parent Topic:**[Create and manage enterprise asset inventory](managing-enterprise-asset-inventory.md)

