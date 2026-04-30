---
title: Sourcing items in a service catalog request
description: A service catalog request can contain multiple items that must be sourced.
locale: en-US
release: zurich
product: Procurement
classification: procurement
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Procurement, Asset Management, IT Service Management]
---

# Sourcing items in a service catalog request

A service catalog request can contain multiple items that must be sourced.

![Methods of sourcing requested items](../image/source_request_type.png "Methods of sourcing requested items")

**Note:** Only items with an assigned model can be sourced. You can’t source bundles.

## Sourcing requested items from local stockrooms

You can use the assets available in the requester’s local stockroom to fulfill a service catalog request. The assets that are in stock are reserved and a fulfillment task is created to source and fulfill the request.

## Sourcing requested items from other stockrooms

When the requested items aren’t in stock, you can create a purchase order to deliver the items from other source stockrooms to your local stockroom. You can request multiple items in a purchase order.

After creating a purchase order, you can create hardware assets and reserve it for the requester either before or after you receive the requested items. You can’t create or assign software licenses to the requester before you receive the software licenses.

## Sourcing requested hardware items

You can source requested hardware items by creating a transfer order. You can transfer hardware assets from a source stockroom to multiple destination stockrooms.

When a source stockroom doesn’t have enough items in stock, you can specify multiple source stockrooms in the transfer order so that the hardware items can be transferred to the destination stockrooms.

**Important:** If the Field Service Management application is also activated on your ServiceNow instance, then a workflow in this application processes the transfer orders. For more information, see [Move an asset through the transfer process](https://www.servicenow.com/docs/access?context=create-transfer-order-line-task&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US).

## Sourcing requested software licenses

To source a requested software license, you must assign the rights of the software license to a user or a device so that they’re authorized to use the software.

-   **[Create a purchase order from a request](../task/t_CreatingPurchOrderFromRequest.md)**  
You can create a purchase order directly from a request. This approach enables procurement managers to obtain items and fulfill requests from the Service Catalog. You can create multiple purchase orders from a request.
-   **[Create a transfer order from a request](../task/t_CreatingTransferOrderFromReq.md)**  
You can create a transfer order directly from a request to source hardware items and consumables from stockrooms.
-   **[Source requests from local stockrooms](../task/consume-local-asset-stock.md)**  
Get visibility into local stockrooms at the time of sourcing requests.
-   **[Add an assignment from a request](../task/t_AddingAssignmentsFromReq.md)**  
You can add assignments directly from a request to source rights from software licenses.

**Parent Topic:**[Procurement](c_Procurement.md)

**Related topics**  


[Procurement roles](../reference/r_ProcurementRoles.md)

[Procurement workflows](c_ProcurementWorkflows.md)

[Use the Procurement Overview module](../task/t_UsingTheProcurementOverviewModule.md)

[Activate Procurement](../task/t_ActivateProcurement.md)

[Procurement purchase order management for assets](c_UseProcurement.md)

[Receive assets](c_ReceiveAssets.md)

[Domain separation and Procurement](domain-separation-procurement.md)

[Manage transfer orders](https://www.servicenow.com/docs/access?context=c_TransferOrders&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)

[Track a request from the service catalog](../task/t_TrackReqFromServiceCatalog.md)

[Models](../../product-catalog/concept/c_Models.md)

[Bundled models](../../product-catalog/concept/c_CreatingBundledModels.md)

[Source requests from local stockrooms](../task/consume-local-asset-stock.md)

