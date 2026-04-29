---
title: Track a request from the service catalog
description: The Procurement application lets you track a request that was ordered from the service catalog.
locale: en-US
release: australia
product: Procurement
classification: procurement
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Procurement purchase order management for assets, Procurement, IT Asset Management]
---

# Track a request from the service catalog

The Procurement application lets you track a request that was ordered from the service catalog.

## Before you begin

Role required: procurement\_admin or procurement\_user

## About this task

When a user places an order from the service catalog, a request record is created to track the order. Each ordered item becomes a requested item that is listed on the request record. For example, a single request for one laptop, two monitors, and one keyboard creates the following records.

Request REQ0000001: 4 items

-   Requested Item RITM0000001: 1 laptop
-   Requested Item RITM0000002: 2 monitors
-   Requested Item RITM0000003: 1 keyboard

## Procedure

1.  Navigate to **All** &gt; **Procurement** &gt; **Requests** &gt; **Requests**.

2.  Click a request **Number**.

    The **Requested Items** related list displays the items that were ordered. You can view the requested item, or view associated **Purchase Orders**, **Transfer Orders**, and **Assignments** on other related lists. A catalog task is automatically generated for each requested item to identify the source of the item, whether it must be purchased or transferred from a stockroom.


**Parent Topic:**[Procurement purchase order management for assets](../concept/c_UseProcurement.md)

**Related topics**  


[Cancel a request from the service catalog](t_CancelReqFromServCatalog.md)

[View and edit a catalog task](t_ViewAndEditACatalogTask.md)

[Create a purchase order](t_CreateAPurchaseOrder.md)

[Create an asset and reserve it for the requester](t_CreateAssetReserveForRequester.md)

