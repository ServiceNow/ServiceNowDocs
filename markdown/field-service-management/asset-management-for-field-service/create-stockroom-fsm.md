---
title: Create stockroom for Field Service Management assets
description: Create a stockroom in the Field Service Management application and assign assets to it.
locale: en-US
release: australia
product: Asset Management for Field Service
classification: asset-management-for-field-service
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Stockrooms, Inventory and asset management, Configure, Field Service Management]
---

# Create stockroom for Field Service Management assets

Create a stockroom in the Field Service Management application and assign assets to it.

## Before you begin

Role required: admin

## About this task

Stockrooms are separate, standalone entities in the Field Service Management application. When stock is low on a particular asset, stock rules can notify an asset manager, or automatically transfer inventory from one stockroom to another. For more information about stock rules, see [Create a stock rule for enterprise assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/create-eamstockrules.md).

## Procedure

1.  Navigate to **All** &gt; **Inventory** &gt; **Stockrooms**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_ahg_41r_41c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Display name and identifier of the stockroom.

</td></tr><tr><td>

Assignment group

</td><td>

Group that primarily uses the stockroom.

</td></tr><tr><td>

Manager

</td><td>

Person in charge of the stockroom. Receives restocking notifications and requests for the stockroom's stock rules.

</td></tr><tr><td>

Location

</td><td>

Physical location of the stockroom.

</td></tr><tr><td>

Type

</td><td>

Type of stockroom. Choose from the following options:-   Central Warehouse
-   Field Agent
-   FSL
-   On site
-   PUDO
-   Warehouse


</td></tr><tr><td>

Hours of operation

</td><td>

Hours during which the stockroom operates.

</td></tr><tr><td>

Description

</td><td>

Description of the stockroom.

</td></tr><tr><td>

Exclude from distribution channels

</td><td>

Option to exclude the stockroom from all stockroom distribution channels, which link stockrooms together for more efficient asset sourcing and transfers.

</td></tr><tr><td>

Exclude from service locations

</td><td>

Option to exclude the stockroom from all service locations in which you are completing work orders or work order tasks.

</td></tr><tr><td>

External

</td><td>

Indicates if this stockroom is managed internally \(check box is cleared\) or is managed externally by a third party \(check box is selected\).

</td></tr></tbody>
</table>4.  Select **Save**.

    The newly created stockroom appears in the **All stockrooms** tab.


