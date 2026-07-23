---
title: Product inventory and closed-loop order fulfillment
description: Sales CRM for Telecommunications instantiates product inventory from the PSR catalog definition used to configure the quote. It manages the product lifecycle through the order, closing the loop between order submission and service activation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/product-inventory-closed-loop-somt.html
release: australia
topic_type: concept
last_updated: "2025-07-14"
reading_time_minutes: 5
keywords: [product inventory, closed loop, order fulfillment, sold product, TMF637, inventory lifecycle, MACD orders, suspend resume disconnect]
breadcrumb: [Explore, Sales Customer Relationship Management for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Product inventory and closed-loop order fulfillment

Sales CRM for Telecommunications instantiates product inventory from the PSR catalog definition used to configure the quote. It manages the product lifecycle through the order, closing the loop between order submission and service activation.

In Sales CRM for Telecommunications, product inventory is not a separate system. When a customer order is approved, the platform creates product inventory records directly from the PSR catalog definition used to configure and price the quote. This means what was sold and what is provisioned always derive from the same source, removing the need to synchronize data between sales and fulfillment systems.

The order manages the inventory record throughout its lifecycle. As domain orders close during fulfillment, inventory states update automatically. When activation feedback returns from downstream provisioning systems, the platform updates the inventory record to reflect the confirmed service state. This closes the loop between order submission and service delivery.

## Benefits

-   Product inventory is instantiated from the same PSR catalog definition used to configure the quote, removing the need to synchronize data between separate sales and fulfillment systems.
-   Inventory state updates automatically as domain orders close during fulfillment, removing the need for manual inventory updates after service activation.
-   A single inventory record tracks the full service lifecycle from Installation Pending through Active, Suspended, and Inactive giving operations teams a consistent view of what is provisioned.
-   Change, suspend, resume, and disconnect orders act directly on product inventory records, so service modifications don't require new catalog entries or manual order construction.
-   Closed-loop activation feedback from downstream provisioning systems updates order and inventory state automatically, reducing manual follow-up between fulfillment and operations teams.
-   TMF637 alignment supports standards-based product inventory management with third-party provisioning systems extends this to the resource order layer.

## Features

|Feature|Description|
|-------|-----------|
|Catalog-driven inventory instantiation|Creates product inventory records from the same PSR catalog definition used to configure and price the quote. Inventory is created at order approval with placeholders for all specifications, and activates as domain orders close during fulfillment.|
|Automatic inventory state management|Transitions inventory records through Installation Pending, Active, Change Pending, Suspended, and Inactive states automatically as the order progresses. No manual inventory updates are required after order approval.|
|MACD order support|Supports modify, add, change, and disconnect \(MACD\) order types directly against product inventory records. Change, suspend, resume, and disconnect orders act on Active or Suspended inventory records without requiring new catalog entries.|
|Closed-loop activation feedback|Receives activation confirmation responses from downstream provisioning systems and uses them to close domain orders, update inventory states, and close the customer order automatically. Reduces manual follow-up between fulfillment and operations teams.|
|TMF637 product inventory alignment|Manages product inventory instantiation and lifecycle in alignment with the TM Forum TMF637 Product Inventory Management API standard. Supports standards-based integration with third-party provisioning and inventory systems.|
|Unified inventory and order visibility|Tracks product inventory state alongside order status, domain order progress, and fulfillment tasks on one platform. Sales and operations teams share a single view of what is sold, what is provisioned, and what is active.|

## Product inventory instantiation

Product inventory records are created and added to the Product Inventory \[sn\_prd\_invt\_product\_inventory\] table after an order is decomposed, completed, and fulfilled. The Product Inventory table extends the Sold Product \[sn\_install\_base\_sold\_product\] table. Product inventory records are created for products with specifications.

The instantiation sequence is as follows:

1.  After the fulfillment manager approves the order, the platform creates a product inventory record with placeholders for all specifications generated after decomposition. The associated models are in an Installation Pending state.
2.  During fulfillment, as product, service, and resource orders close, the state of each associated specification updates to Active in the product inventory record.
3.  When the customer order closes, all characteristics associated with the specifications on the customer order update the inventory record.

**Note:** Depending on how the **sn\_ind\_tmt\_orm.enable\_prod\_invt\_for\_order\_management** system property is configured, the platform creates either sold product records or product inventory records. Only product inventory records support change, disconnect, suspend, and resume order types.

## Inventory lifecycle states

The product inventory record transitions through the following states as the order progresses:

|State|Description|
|-----|-----------|
|Installation Pending|Record created at order approval. Placeholders exist for all specifications. The inventory record does not affect service availability at this stage.|
|Active|All associated domain orders are closed and fulfillment is confirmed. Specifications update to Active and the inventory record reflects the live service state.|
|Change Pending|A change order is approved. Changed or removed specifications update to Change Pending until the change order fulfillment completes.|
|Suspended|A suspend order is fulfilled. The inventory record transitions from Active to Suspended after all associated tasks and jobs complete.|
|Inactive|A disconnect order is fulfilled. The inventory record moves to Inactive after the order completes. Disconnect orders can be created for records in Active or Suspended states.|

## Order types that act on product inventory

Product inventory records support the following order types for managing the customer service lifecycle after initial activation:

|Order type|Description|
|----------|-----------|
|Change|Modifies an existing product or service. Changed specifications transition to Change Pending during fulfillment and return to Active on completion.|
|Suspend|Temporarily deactivates a product or service. The inventory record transitions from Active to Suspended after all tasks and jobs complete.|
|Resume|Reactivates a suspended product or service. The inventory record transitions from Suspended back to Active after all tasks and jobs complete.|
|Disconnect|Permanently deactivates a product or service. The inventory record moves to Inactive after the order completes. Available for records in Active or Suspended states.|

## Closed-loop order fulfillment

Closed-loop fulfillment connects order submission to service activation confirmation. When downstream provisioning systems complete activation, they return a response to Sales CRM for Telecommunications. The platform uses this response to update domain order states, close the associated order tasks, and transition the product inventory record to Active without manual intervention.

This closed loop covers the following stages:

-   Order decomposition generates domain orders and routes them to fulfillment systems.
-   Fulfillment systems activate the service and return a confirmation response.
-   The platform closes the domain order and updates the associated product inventory specification to Active.
-   When all domain orders close, the customer order closes and the inventory record reflects the fully activated service.

Sales CRM for Telecommunications aligns closed-loop fulfillment to TM Forum Open API standards. TMF637 manages product inventory instantiation and lifecycle. TMF641 manages service order routing and activation responses.

