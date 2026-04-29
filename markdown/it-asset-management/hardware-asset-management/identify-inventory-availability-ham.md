---
title: Identify suitable replacement options for assets in the Hardware Asset Workspace
description: Use the Inventory availability report to determine suitable replacement options for your assets and their child components that are in use, in maintenance, pending repair, or defective. The report also helps you to determine the quantity of available substitute models that can be used locally, moved through the distribution channels, and estimate the lead time for new purchases.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage stockrooms with inventory reports in the Hardware Asset Workspace, Manage stockrooms, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Identify suitable replacement options for assets in the Hardware Asset Workspace

Use the Inventory availability report to determine suitable replacement options for your assets and their child components that are in use, in maintenance, pending repair, or defective. The report also helps you to determine the quantity of available substitute models that can be used locally, moved through the distribution channels, and estimate the lead time for new purchases.

## Before you begin

The Inventory Availability Report is available only for hardware, consumable, and bundle assets that are in use, in maintenance, pending repair, or defective.

Service locations and distribution channels should be configured for the stockroom. If the asset's location is a service location of a stockroom, it automatically becomes the local stockroom. A location can have multiple local stockrooms if it is serviced by more than one stockroom. For more details, see [Associate a stockroom with service locations](associate-stockroom-with-service-locations.md) and [Link stockrooms into a distribution channel](associate-stockroom-with-distribution-channels.md).

Role required: asset

## About this task

The Inventory availability report helps you to identify the best sourcing option when sourcing assets or its components that are in use and nearing the end of their life, defective, or pending repair. Additionally, you can check how much stock is currently available at a stockroom.

## Procedure

1.  Navigate to **Workspaces** &gt; **Hardware Asset Workspace** &gt; **Asset estate**.

2.  Select the asset for which you want to view the replacement assets available in the local and remote stockrooms.

3.  Select the **Inventory availability** tab.

    The list displays the asset and any of its child assets, along with their linked models and any substitute models. The list includes the following details:

<table id="table_n5d_jqm_sfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Asset

</td><td>

Display name of the asset.

</td></tr><tr><td>

Model

</td><td>

Model of the asset.**Note:** If there are any substitute models for the asset model, they’re also displayed.

</td></tr><tr><td>

Asset type

</td><td>

Indicates whether the asset is the original asset or a substitute model asset.This field can have any of the following values:

-   **Original parent** for the actual parent asset.
-   **Original child** for the child of the original parent asset.
-   **Substitute parent** for the asset of the substitute model.
-   **Substitute child** for the child asset of the substitute model.


</td></tr><tr><td>

Local stockroom quantity

</td><td>

Quantity of assets that are in stock and available in the stockrooms that service the asset location.**Note:**

If you select the quantity shown, you can view the full list of assets in your local stockroom that can be used as replacements. There can be multiple local stockrooms if more than one stockroom serves the same location.

</td></tr><tr><td>

Remote stockroom quantity

</td><td>

Quantity of assets that are in stock and available in the distribution channel stockrooms that are marked as inbound stockrooms to the current local stockroom.**Note:**

If you select the quantity shown, you can view the full list of assets in your distribution channel stockrooms that can be used as replacements.

</td></tr><tr><td>

Purchase lead time

</td><td>

Average time in days it has taken from ordering to receiving replacement assets through new purchase orders.

</td></tr></tbody>
</table>
**Parent Topic:**[Manage stockrooms with inventory reports in the Hardware Asset Workspace](../concept/manage-stockroom-inventory-report-ham.md)

