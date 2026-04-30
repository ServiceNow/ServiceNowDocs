---
title: Receiving enterprise and consumable assets at stockrooms
description: As an enterprise asset manager or enterprise asset technician, you can receive assets at a stockroom from any workflow using the unified and standardized receiving mechanism.
locale: en-US
release: yokohama
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2025-06-22"
reading_time_minutes: 2
breadcrumb: [Exploring Enterprise Asset Management, Enterprise Asset Management, IT Asset Management]
---

# Receiving enterprise and consumable assets at stockrooms

As an enterprise asset manager or enterprise asset technician, you can receive assets at a stockroom from any workflow using the unified and standardized receiving mechanism.

**Important:** The standardized asset receiving mechanism is available with Enterprise Asset Management version 9.0 and later.

With the standardized receiving process, you don't need to be familiar with the specific workflow to which the assets belong. Therefore, you can receive hardware and consumable assets from different shipments originating from sources, like transfer orders, purchase orders, or any other workflows seamlessly.

## Requirements and limitations

-   You can receive enterprise assets in the Hardware Asset Workspace only if the Enterprise Asset Management applications is activated.
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

