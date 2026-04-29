---
title: View and edit a catalog task
description: Catalog tasks are used to source items and fulfill requests. You can view and edit catalog tasks from a request.
locale: en-US
release: australia
product: Procurement
classification: procurement
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Procurement purchase order management for assets, Procurement, IT Asset Management]
---

# View and edit a catalog task

Catalog tasks are used to source items and fulfill requests. You can view and edit catalog tasks from a request.

## Before you begin

Role required: procurement\_admin or procurement\_user

## About this task

If a request requires approval, a catalog task is created automatically when the request is approved. If a request doesn’t require approval, a catalog task is created automatically when the request is created.

**Note:** If a request contains one requested item and the item has no model specified, a catalog task isn’t created automatically. If a request includes multiple items and only some have a specified model, catalog tasks are automatically created, but only for those items with a model.

## Procedure

1.  Navigate to **All** &gt; **Procurement** &gt; **Requests** &gt; **Tasks**.

2.  Open a catalog task.

3.  Edit the fields as necessary.

    |Field|Description|
    |-----|-----------|
    |Number|The unique number identifying the catalog task.|
    |Request|The number of the request to which the catalog task is associated. The information in this field is derived from the **Number** field on the Request form.|
    |Request item|The number of the requested item to which the catalog task is associated. The information in this field is derived from the **Number** field on the Requested Item form.|
    |Requested for|The name of the person for whom the associated item was requested. The information in this field is derived from the **Request** or **Request item** field.|
    |Due date|The date by which the catalog task should be completed.|
    |Configuration item|The configuration item associated with the **Request Item**.|
    |Approval|The status of catalog task approval: **Not Yet Requested**, **Requested**, **Approved**, or **Rejected**.|
    |State|The current state of the catalog task: **Pending**, **Open**, **Work in Progress**, **Closed Complete**, **Closed Incomplete**, or **Closed Skipped**.|
    |Assignment group|The group from which an individual is selected to complete the catalog task.|
    |Assigned to|The individual assigned to complete the catalog task is selected from the **Assignment group**.|
    |Work notes list|The list of users to receive email notifications when the work notes on the catalog task are updated.|
    |Short description|A brief description of the catalog task.|
    |Description|A detailed description of the catalog task.|
    |Work notes|Information about how the catalog task is resolved.|
    |Parent|The parent record associated with the task.|
    |Additional comments|Additional information about the catalog task.|

4.  Select **Update**.


**Parent Topic:**[Procurement purchase order management for assets](../concept/c_UseProcurement.md)

**Related topics**  


[Track a request from the service catalog](t_TrackReqFromServiceCatalog.md)

[Cancel a request from the service catalog](t_CancelReqFromServCatalog.md)

[Create a purchase order](t_CreateAPurchaseOrder.md)

[Create an asset and reserve it for the requester](t_CreateAssetReserveForRequester.md)

[Models](../../product-catalog/concept/c_Models.md)

