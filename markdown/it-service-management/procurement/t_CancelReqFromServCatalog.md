---
title: Cancel a request from the service catalog
description: You can cancel a request from the service catalog if, for example, the item is no longer needed or the request was not approved.
locale: en-US
release: xanadu
product: Procurement
classification: procurement
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Procurement purchase order management for assets, Procurement, Asset Management, IT Service Management]
---

# Cancel a request from the service catalog

You can cancel a request from the service catalog if, for example, the item is no longer needed or the request was not approved.

## Before you begin

Role required: catalog\_admin, procurement\_admin, or procurement\_user

## About this task

When a service catalog request is canceled, the following actions occur automatically.

-   Associated purchase orders that have not been received are canceled.
-   All procurement tasks are canceled.
-   Associated transfer orders are canceled, if all transfer order lines related to the transfer order are also associated with the service catalog request and the transfer order lines have all been canceled. If the transfer order contains transfer order lines that are not related to the service catalog request and those lines have not been canceled, the transfer order is not canceled.

Associated transfer order lines that are in the **In Transit** or **Delivered** stages are not canceled.

## Procedure

1.  Navigate to **All** &gt; **Procurement** &gt; **Requests** &gt; **Requests**.

2.  Click a request **Number**.

3.  Click **Cancel Request**.


**Parent Topic:**[Procurement purchase order management for assets](../concept/c_UseProcurement.md)

**Related topics**  


[Consumable assets](../concept/c_ReceiveAConsumableAsset.md)

[Track a request from the service catalog](t_TrackReqFromServiceCatalog.md)

[View and edit a catalog task](t_ViewAndEditACatalogTask.md)

[Create a purchase order](t_CreateAPurchaseOrder.md)

[Create an asset and reserve it for the requester](t_CreateAssetReserveForRequester.md)

