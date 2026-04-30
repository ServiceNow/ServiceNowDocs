---
title: Create an asset and reserve it for the requester
description: Create the asset before they're delivered so that you can create the asset record with an asset tag and serial number early in the process and reserve the asset for the user who requested it. The receiver can only select the assets to be received as assets are pre-created.
locale: en-US
release: xanadu
product: Procurement
classification: procurement
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Procurement purchase order management for assets, Procurement, Asset Management, IT Service Management]
---

# Create an asset and reserve it for the requester

Create the asset before they're delivered so that you can create the asset record with an asset tag and serial number early in the process and reserve the asset for the user who requested it. The receiver can only select the assets to be received as assets are pre-created.

## Before you begin

Role required: procurement\_admin or procurement\_user

## About this task

Some requests must be approved before items on the request can be sourced. In the base system, requests over $1,000 require approval. To change the $1,000 approval threshold and other workflow attributes, edit the Service Catalog Request workflow.

When the asset state is **In stock**, the **Reserved for** field is maintained as the asset is received and placed in a stockroom. When the asset state changes to **In use**, the **Reserved for** field is relabeled **Assigned to**. If there is a name in the **Reserved for** field, the name is retained when the field is relabeled. A user with the asset role can change the name in the **Assigned to** field. Changing the name is helpful, for example, if an IT technician orders 10 laptops and must assign them to individual users.

**Note:** If assets are not created prior to delivery, they are automatically created from line items when purchase orders are received. Also you can enter the asset details and receive them when the purchase orders are received.

## Procedure

1.  Navigate to **All** &gt; **Procurement** &gt; **Requests** &gt; **Tasks**.

2.  Open a task with a **State** of **Open** and a **Short description** of **Source Request Items**.

3.  Click **Source Request**.

    -   If the request is already fulfilled or the items in the request are not sourceable, the **Source Request** button is hidden.
    -   If the requested item does not have an assigned model, the item is not listed on the Source the Request dialog box.
    -   Any items on the purchase order that have a remaining quantity of **0** are not listed on the Source the Request dialog box.
4.  Select a **Destination Stockroom**.

5.  Select the **Create PO** option for one or more listed items.

6.  For each item requiring a purchase order, select a **Vendor**.

7.  Click **OK**.

8.  Navigate to **Procurement** &gt; **Orders** &gt; **Purchase Orders**.

9.  Open the purchase order you just created.

    If you created a purchase order for more than one item, multiple purchase orders may have been created.

10. Select **Order**.

    After the items are ordered, no additional purchase order line items can be added to the purchase order.

    The status of all purchase order line items changes to **Ordered**.

11. Click the **Create hardware assets prior to delivery** related link to automatically create hardware assets for all purchase order line items.

    Hardware assets are listed in the **Assets** related list. Click an asset in the list to view the asset record. Except for consumables, the **Reserved for** field contains the name of the user who made the original request.

    You can also create assets for individual purchase order line items. On a purchase order, go to the **Purchase order line items** related list and click a specific purchase order line item number. Then, click the **Create hardware assets prior to delivery** related link. Only the hardware assets included on the purchase order line item are created.


**Parent Topic:**[Procurement purchase order management for assets](../concept/c_UseProcurement.md)

**Related topics**  


[Consumable assets](../concept/c_ReceiveAConsumableAsset.md)

[Track a request from the service catalog](t_TrackReqFromServiceCatalog.md)

[Cancel a request from the service catalog](t_CancelReqFromServCatalog.md)

[View and edit a catalog task](t_ViewAndEditACatalogTask.md)

[Create a purchase order](t_CreateAPurchaseOrder.md)

[](https://www.servicenow.com/docs/access?context=workflow-editor&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)

[Set asset states and substates](../../asset-management/task/t_SettingAssetStatesAndSubstates.md)

[Models](../../product-catalog/concept/c_Models.md)

