---
title: Creation of sold product and product inventory records
description: Learn how the Order Management application creates and maintains the customer product and service inventory. By using this application, you can maintain an accurate inventory of your customer products and services.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Order fulfillment, Order Management, Use, Sales Customer Relationship Management]
---

# Creation of sold product and product inventory records

Learn how the Order Management application creates and maintains the customer product and service inventory. By using this application, you can maintain an accurate inventory of your customer products and services.

## Customer product data record creation

Sold product records are created and added to the Sold Product \[sn\_install\_base\_sold\_product\] table after an order line is marked as closed complete. Product inventory records are created and added to the Product Inventory \[sn\_prd\_invt\_product\_inventory\] table after an order is decomposed, completed, and fulfilled. Product inventory records are created for products with specifications. Depending on how your admin has configured the sn\_ind\_tmt\_orm.enable\_prod\_invt\_for\_order\_management system property, either sold products or product inventory records are created. For more information, see [Configure customer product data management](../../customer-service-management/task/configure-customer-product-data-management.md).

The Product Inventory table extends the Sold Product table. Only the items from the product inventory are available for change, disconnect, suspend, or resume type orders.

## New order workflow

The new order workflow is as follows:

1.  After the fulfillment or service order manager approves the order, the product inventory record is created. This record has placeholders for all the specifications that are generated after decomposition. The associated models have an Installation Pending state.
2.  During the fulfillment process, when the product, service, and resource orders are closed, the state of the associated specification updates to Active in the product inventory record.
3.  When you close the customer order, all the characteristics that are associated with the specifications on the customer order update the record.

## Change order workflow

The change order workflow is as follows:

1.  After the fulfillment manager or service order approves the order, the state of the changed or removed specifications are updated to Change Pending. The models that are associated with the changed specifications are also updated to reflect the latest model that is generated due to the change.
2.  During the fulfillment process, when the product, service, and resource orders are closed, the state of the associated specification updates to Active.
3.  When you close the customer order, all the characteristics that are associated with the specifications on the customer order update the record.
4.  If the change order included a request to disconnect a product or service, the associated product inventory record moves to an Inactive state after the order is complete.

    You can create orders with action type as disconnect for product inventory records that are in Active or Suspended states.

    For suspend type orders, the end state is Suspended after the suspend workflow is completed. Product inventory state changes from Active to Suspended after all tasks and jobs have finished.

    For resume type orders, the end state is Active after the resume workflow is completed. Product inventory state changes from Suspended back to Active after all tasks and jobs have finished.


**Parent Topic:**[Order fulfillment](reviewing-orchestration-plans-order-fulfillment.md)

**Related topics**  


[Customer Life Cycle Management Workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customer-life-cycle-management-workflows.md)

[Managing post-fulfillment order changes](managing-orders.md)

[Request post-sale change orders](../task/create-macd-orders.md)

