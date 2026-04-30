---
title: Create stockroom for enterprise assets
description: Create a stockroom in the Enterprise Asset Management application and assign assets to it.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create and manage enterprise asset inventory, Managing enterprise asset inventory and contracts, Enterprise Asset Management, IT Asset Management]
---

# Create stockroom for enterprise assets

Create a stockroom in the Enterprise Asset Management application and assign assets to it.

## Before you begin

Role required: sn\_eam.enterprise\_admin or sn\_eam.enterptrise\_asset\_manager

## Procedure

1.  Navigate to **Enterprise Asset Workspace** &gt; **Inventory** &gt; **All stockrooms**.

2.  Select **New**.

    The Create New Stockroom page opens.

3.  On the form, fill in the fields.

<table id="table_dhx_jt2_psb"><thead><tr><th>

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


-   **[Add a distribution channel to a stockroom in the Enterprise Asset Workspace](add-distribution-channel-eam-stockroom.md)**  
Add a distribution channel to a stockroom so that you can link that stockroom with other geographically-related stockrooms. By linking your stockrooms, you can efficiently source and transfer assets between those stockrooms. You can also assign a rank to each linked stockroom to specify the order of stockrooms that you can source and transfer assets between.
-   **[Add service locations to a stockroom in the Enterprise Asset Workspace](add-service-location-eam-stockroom.md)**  
Add service locations to a stockroom so that you can source, deploy, and retire its assets across multiple geographic locations.

**Parent Topic:**[Create and manage enterprise asset inventory](../concept/managing-enterprise-asset-inventory.md)

