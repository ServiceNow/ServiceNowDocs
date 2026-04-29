---
title: Inventory view
description: Use the Inventory view in the Hardware Asset Workspace to view the inventory functions such as Asset audits and Disposal orders and to take any inventory-related actions.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Hardware Asset Workspace, Exploring Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Inventory view

Use the Inventory view in the Hardware Asset Workspace to view the inventory functions such as Asset audits and Disposal orders and to take any inventory-related actions.

Use the following tabs to view the inventory functions and take appropriate actions:

-   **Overview**: View various inventory data, such as the number of open hardware requests from stock, RMA request lines, and open transfer orders.
-   **All stockrooms**: View, create, and manage stockrooms.
-   **Asset audits**: Perform scheduled or blind audits of asset stockrooms and other locations such as offices or data centers.
-   **Disposal orders**: Create and manage a disposal order for hardware or consumable assets that have reached their end of life cycle or are no longer functional.
-   **Loaner asset orders**: View all the Loaner asset orders and take appropriate actions.
-   **RMA orders**: View all the RMA orders and take appropriate actions.
-   **RMA line items**: View all the RMA line items and take appropriate actions.
-   **Transfer orders**: Create transfer orders, view existing transfer orders, and take appropriate actions.
-   **Donation orders**: View the list of asset donation orders.
-   **Repair orders**: View the list of repair orders submitted for repair of assets with your stockroom. You can also create repair orders.

To create an asset audit for your inventory, select **New asset audit**. For more details, see [Create an audit record in the Hardware Asset Management application](../task/audit-your-inventory.md).

**Note:** You need the asset or inventory\_admin role to access the Inventory view.

## Overview tab

Use the **Overview** tab for a consolidated view of various inventory data as widgets. You can also view notifications about actions with links to act on discrepancies, such as incomplete information on asset audits or disposal orders.

![Inventory view in Hardware Asset Workspace.](../image/inventory-view.png "Inventory view")

Select any widget or chart to view in detail and take required actions. You can also use **Domain**, **Location**, **Stockroom**, and **Model category** lists to narrow down your results. The **Domain** filter is available only when domain separation is enabled.

|Widget or chart|Description|
|---------------|-----------|
|Open hardware requests from stock \(YTD\)|Number of transfer orders of Procurement type that are already delivered and created this calendar year.|
|Open RMA request lines|Number of open RMA request lines.|
|Open transfer orders|Number of canceled or undelivered transfer orders.|
|Open asset audits|Number of asset audits that are currently new or in progress.|
|Open stock orders|Number of incomplete or canceled stock orders.|
|Orders pending delivery by stockroom|Number of purchase orders that aren’t received or canceled.|
|Active stock rules by model category|All active stock rules grouped by their model category.|
|Loaner asset orders by status|Number of loaner asset orders grouped by their status, such as Return overdue, Deployed, and New.|

You can use the following important action cards related to service locations, distribution channels, and shipments to view the list of items that needs your action:

-   Stockrooms missing service locations: List of stockrooms that aren’t associated with any service locations. Stockrooms that are excluded from providing support to service locations aren't shown in the list.
-   Stockrooms missing distribution channels: List of stockrooms that aren’t associated with any distribution channels. Stockrooms that are excluded from having distribution channels aren't shown in the list.
-   Stale shipments: List of shipments that weren’t updated with the tracking information from the integrated carrier.
-   Shipment data discrepancy: List of shipment records with the Carrier status as delivered and the Stage as In Transit.
-   Carrier integration failures: List of integration profiles that failed to connect three consecutive times.
-   Unmapped carrier profiles: List of integration profiles that aren’t associated with a carrier.

**Note:** You can view **Stale shipments**, **Carrier integration failures**, and **Unmapped carrier profiles** important action cards with asset, inventory\_admin, or ham\_admin role.

