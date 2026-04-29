---
title: View stockroom details in the Enterprise Asset Workspace
description: Use stockroom records to view detailed information about the stockrooms that your enterprise, hardware, consumable, bundle, loaner, and other assets reside in.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Create and manage enterprise asset inventory, Managing enterprise asset inventory and contracts, Enterprise Asset Management, IT Asset Management]
---

# View stockroom details in the Enterprise Asset Workspace

Use stockroom records to view detailed information about the stockrooms that your enterprise, hardware, consumable, bundle, loaner, and other assets reside in.

## Before you begin

The following stockroom record tabs are available only if you've installed and activated the Hardware Asset Management application on your ServiceNow® instance:

-   **Hardware**
-   **Bundles**
-   **Software Licenses**
-   **Other Assets**
-   **Hardware Loaner Pool**
-   **Hardware Asset Audits**

To install and activate the application, request it from the [ServiceNow Store](https://store.servicenow.com).

Role required: sn\_eam.enterprise\_admin, sn\_eam.enterptrise\_asset\_manager, or enterprise\_asset\_technician

## Procedure

1.  From the Enterprise Asset Workspace, open the Inventory view.

2.  Select the **All stockrooms** tab.

3.  From the list of available stockrooms, select the stockroom for which you want to view additional details.

    The stockroom record opens.

4.  Use the stockroom record tabs to view additional details about the stockroom.

<table id="table_zc2_pym_gxb"><thead><tr><th>

Tab

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Details

</td><td>

Get a detailed overview of the stockroom, including open stockroom tasks and general stockroom details.

 The Open stockroom tasks cards show all open orders, audits, and requests that are associated with the stockroom. Select a card to view the list of corresponding order, audit, or request records. If you select a card for any open Hardware Asset Management orders, audits, or requests, the list opens in the Hardware Asset Workspace.

 In addition, use the interactive map to view the location of the stockroom based on the specified stockroom address. Expand the map to view all supported service locations and all stockrooms that are linked as part of the stockroom distribution channel.

</td></tr><tr><td>

Task Timeline

</td><td>

View the timeline of all stockroom tasks. Each stockroom task is added to the timeline based on either the creation date, the scheduled date, the start or return date, or the shipping date. Select a task to open the corresponding task record. If you select a Hardware Asset Management task, the record opens in the Hardware Asset Workspace.

 Use the timeline format filter at the top-right corner of the tab to change the format and duration in which you view the timeline. You can choose to view the timeline in a calendar format or timeline format. The calendar format supports the following timeline durations:

-   **Day**
-   **Work Week**
-   **Week**
-   **Month**
 The timeline format supports the following timeline durations:

-   **Day**
-   **Week**
-   **4 Weeks**


</td></tr><tr><td>

Hardware**Note:** This tab appears only if you have installed and activated the Hardware Asset Management application.

</td><td>

Create and view the hardware assets that reside in the stockroom.

 If you are creating a hardware asset, you are automatically redirected to the corresponding form in the Hardware Asset Workspace.

</td></tr><tr><td>

Enterprise Assets

</td><td>

Create and view the enterprise assets that reside in the stockroom.

</td></tr><tr><td>

Consumables

</td><td>

Create and view the consumable assets that reside in the stockroom.

</td></tr><tr><td>

Bundles**Note:** This tab appears only if you have installed and activated the Hardware Asset Management application.

</td><td>

Create and view the asset bundles that reside in the stockroom.

 If you are creating an asset bundle or selecting an existing asset bundle, you are automatically redirected to the corresponding form or record in the Hardware Asset Workspace.

</td></tr><tr><td>

Pallets

</td><td>

Create and view the pallet assets that reside in the stockroom.

</td></tr><tr><td>

Software Licenses**Note:** This tab appears only if you have installed and activated the Hardware Asset Management application.

</td><td>

Create and view the software licenses that reside in the stockroom.

 If you are creating a software license or selecting an existing software license, you are automatically redirected to the corresponding form or record in the Hardware Asset Workspace.

</td></tr><tr><td>

Other Assets**Note:** This tab appears only if you have installed and activated the Hardware Asset Management application.

</td><td>

Create and view all other types of assets that reside in the stockroom.

 If you are creating an asset, you are automatically redirected to the corresponding form in the Hardware Asset Workspace.

</td></tr><tr><td>

Hardware Loaner Pool**Note:** This tab appears only if you have installed and activated the Hardware Asset Management application.

</td><td>

View all hardware loaner assets that reside in the stockroom.

 If you select a loaner asset, you are automatically redirected to the corresponding record in the Hardware Asset Workspace.

</td></tr><tr><td>

Enterprise Loaner Pool

</td><td>

View all enterprise loaner assets that reside in the stockroom.

</td></tr><tr><td>

Service Locations

</td><td>

View all service locations that are supported by the stockroom.

</td></tr><tr><td>

Distribution Channel

</td><td>

Create and view the list and ranking of all linked stockrooms that you can source and transfer enterprise assets between. For more information on distribution channels, see [Add a distribution channel to a stockroom in the Enterprise Asset Workspace](add-distribution-channel-eam-stockroom.md).

</td></tr><tr><td>

Hardware Asset Audits**Note:** This tab appears only if you have installed and activated the Hardware Asset Management application.

</td><td>

Create and view audits for your hardware asset inventory.

 If you are creating an audit or selecting an existing audit, you are automatically redirected to the corresponding form or record in the Hardware Asset Workspace.

</td></tr><tr><td>

Enterprise Asset Audits

</td><td>

Create and view audits for your enterprise asset inventory.

</td></tr></tbody>
</table>5.  View all active stock rules that are configured for the stockroom.

    1.  From the sidebar of the stockroom record, select the Stock rules icon ![](../image/stock-rules-icon.png).

    2.  View each stock rule to determine if your available stock is within the specified threshold.

        You can also determine if the corresponding model has reached the end of sale.


**Parent Topic:**[Create and manage enterprise asset inventory](../concept/managing-enterprise-asset-inventory.md)

