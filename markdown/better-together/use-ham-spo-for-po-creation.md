---
title: Enhancing the asset procurement experience using IT Asset Management \(ITAM\) and Sourcing and Procurement Operations \(SPO\)
description: Integrating IT Asset Management \(ITAM\) with Sourcing and Procurement Operations \(SPO\) enhances the procurement process for service requests.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Solutions]
---

# Enhancing the asset procurement experience using IT Asset Management \(ITAM\) and Sourcing and Procurement Operations \(SPO\)

Integrating IT Asset Management \(ITAM\) with Sourcing and Procurement Operations \(SPO\) enhances the procurement process for service requests.

## Combined benefits of integrating IT Asset Management and Sourcing and Procurement Operations

Integrating ITAM with SPO provides the following benefits:

-   Streamlines workflows and improves the experience for asset managers and end users.
-   Enables asset managers to initiate and manage external purchases directly from ITAM.
-   Improves data integrity and compliance through synchronized records.
-   Delivers faster, asset-driven procurement with fewer manual steps.
-   Manages receipts, shipments, and assets automatically and consistently across Asset Management \(ALM\) and SPO.

<table id="table_ad3_gmx_ygc"><thead><tr><th>

Feature

</th><th>

IT Asset Management

</th><th>

Sourcing and Procurement Operations

</th><th>

All applications together

</th></tr></thead><tbody><tr><td>

Raise sourcing requests for catalog items without a price

</td><td>

![No](../../reuse/images/icon-error-red-x.png)

</td><td>

![Yes](../../reuse/images/icon-check-mark-green.png)

</td><td>

![Yes](../../reuse/images/icon-check-mark-green.png)

</td></tr><tr><td>

Generate purchase requests for catalog items with a price

</td><td>

![No](../../reuse/images/icon-error-red-x.png)

</td><td>

![Yes](../../reuse/images/icon-check-mark-green.png)

</td><td>

![Yes](../../reuse/images/icon-check-mark-green.png)

</td></tr><tr><td>

Submit asset requests from Employee Center or Service Catalog

</td><td>

![Yes](../../reuse/images/icon-check-mark-green.png)

</td><td>

![No](../../reuse/images/icon-error-red-x.png)

</td><td>

![Yes](../../reuse/images/icon-check-mark-green.png)

</td></tr><tr><td>

Create requests via stock replenishment rules

</td><td>

![Yes](../../reuse/images/icon-check-mark-green.png)

</td><td>

![No](../../reuse/images/icon-error-red-x.png)

</td><td>

![Yes](../../reuse/images/icon-check-mark-green.png)

</td></tr><tr><td>

Receive assets using mobile barcode scanning

</td><td>

![Yes](../../reuse/images/icon-check-mark-green.png)

</td><td>

![No](../../reuse/images/icon-error-red-x.png)

</td><td>

![Yes](../../reuse/images/icon-check-mark-green.png)

</td></tr><tr><td>

Generate comprehensive records in the Asset \[alm\_asset\], Software License \[alm\_license\], and Consumable \[alm\_consumable\] table

</td><td>

![Yes](../../reuse/images/icon-check-mark-green.png)

</td><td>

![No](../../reuse/images/icon-error-red-x.png)

</td><td>

![Yes](../../reuse/images/icon-check-mark-green.png)

</td></tr></tbody>
</table>## Workflow for IT Asset Management and Sourcing and Procurement Operations better together feature

Using the IT Asset Management and Sourcing and Procurement Operations applications together provides the following benefits:

-   Create and manage external purchase by accessing the items from the Shopping Hub within the IT Asset Management application.
-   Manage all related receipts and shipments automatically and consistently across IT Asset Management and Sourcing and Procurement Operations applications.

![ITSM-SPO better together flow](../image/itam-spo-bt-workflow.png "The IT Asset Management and Sourcing and Procurement Operations workflow")

In this workflow:

1.  The procurement journey begins with one of the following events:
    -   An employee requests IT assets through the Service Catalog.
    -   An automated inventory stock order is generated based on stock rule configurations.
2.  The Procurement Manager checks whether the request can be fulfilled with items from local stock, by transferring items, or by placing an order.

3.  The Procurement Manager with the following roles can create a Purchase Order by accessing the items with or without a price from the Shopping Hub catalog to fulfill the service request.
    -   procurement\_admin or procurement\_user
    -   asset manager role \(sn\_spend\_asset.spo\_shopper\)
4.  After the Purchase Order is completed, the requested assets are received and delivered to the stockroom.
5.  In the IT Asset Management application, assets are created when you confirm receipt of the requested items. Depending on the type of the asset, one of the following asset records is created:
    -   For hardware or enterprise assets, a record is added to the Asset \[alm\_asset\] table.
    -   For software assets, an entitlement is created in the Software License \[alm\_license\] table.
    -   For consumable assets, an entitlement is created in the Consumable \[alm\_consumable\] table.

## Requirements for integrating IT Asset Management and Sourcing and Procurement Operations

The following plugins are required to use the IT Asset Management Integration for Sourcing and Procurement Operations better together feature:

1.  IT Asset Management Integration for Sourcing and Procurement Operations \(com.snc.sn\_spend\_asset\) plugin
2.  Sourcing and Purchasing Automation \(com.snc.sn\_pr\) plugin
3.  Procurement \(com.snc.procurement\) plugin
4.  Shopping Hub \(com.snc.uib.sn\_spend\_uib\) plugin

The following additional plugins are required based on the specific IT Asset Management products installed:

-   Enterprise Asset Management \(com.sn\_eam\) plugin
-   Hardware Asset Management \(com.sn\_hamp\) plugin
-   Software Asset Management \(com.snc.samp\) plugin

## Get started with procuring assets from the Shopping Hub catalog

Start procuring assets by accessing the items from the Shopping Hub catalog by completing these tasks:

1.  [Activate Asset Management Integration for Sourcing and Procurement Operations \(sn\_spend\_asset\) plugin](https://store.servicenow.com/store/app/3a2a560a1b8baad02ca2a643604bcb7b).
2.  Begin sourcing and procuring of the requested items from the IT Asset Management workspaces such as Software Asset Workspace, Hardware Asset Workspace, or Enterprise Asset Workspace. For more information, see Create Sourcing Request or Purchase Requisition in SPO via IT Asset Management workspace.
3.  Receive the requested assets in a stockroom. For more information, see Receiving assets in the IT Asset Management application.
4.  Acknowledge the receipt of the assets in the stockroom for asset creation. For more information, see Asset creation in the IT Asset Management application.

**Parent Topic:**[Solutions](../reference/solutions-gallery.md)

