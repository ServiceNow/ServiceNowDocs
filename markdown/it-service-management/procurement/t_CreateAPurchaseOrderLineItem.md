---
title: Create a purchase order line item
description: After you save a new purchase order, you create purchase order line item records to specify the individual items to order.
locale: en-US
release: australia
product: Procurement
classification: procurement
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Create a purchase order, Procurement purchase order management for assets, Procurement, Asset Management, IT Service Management]
---

# Create a purchase order line item

After you save a new purchase order, you create purchase order line item records to specify the individual items to order.

## Before you begin

Role required: procurement\_admin or procurement\_user

## Procedure

1.  Navigate to **All** &gt; **Procurement** &gt; **Orders** &gt; **Purchase Orders**.

2.  Open a purchase order.

3.  In the **Purchase order line items** related list, click **New**.

4.  Complete the form.

<table id="table_rkq_gwx_wq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

The unique number identifying the purchase order line item.

</td></tr><tr><td>

Vendor

</td><td>

The supplier from which this product should be ordered.

</td></tr><tr><td>

Product Model

</td><td>

The model of the purchase order line item.

</td></tr><tr><td>

Product Catalog

</td><td>

The product catalog category to which the product model is assigned. For example, **Hardware**, **Software**, or **Supplies**.

</td></tr><tr><td>

Part number

</td><td>

The identification number assigned to the product model.

</td></tr><tr><td>

Metric group

</td><td>

Each metric group has a set of license metrics that are specific to the software publisher.**Note:** If you select only a software model in the Product model field, this field gets displayed on the form.

</td></tr><tr><td>

License metric

</td><td>

License metric for the license group that the software license is counted against when reconciliation is run. The options for license metric change based on the **Metric group** field. **Note:**

-   If you select only a software model in the Product model field, this field gets displayed on the form.
-   If you choose a license metric that isn't available on Coupa, the license metric value is defaulted as **each**.


</td></tr><tr><td>

Request line

</td><td>

The identification number of the requested item record associated with this purchase order line item.

</td></tr><tr><td>

Ordered

</td><td>

The date and time at which this purchase order line item was ordered.

</td></tr><tr><td>

Expected delivery

</td><td>

The date the purchase order line item is expected to arrive in the stockroom identified in the **Ship to** field on the purchase order record. This field is automatically filled with the value in the **Expected delivery** field on the purchase order record. This field can be edited when the purchase order line item has a **Status** of **Requested**. For more information about this field, see [Purchase order expected delivery date](../reference/r_SetExpectDelDateOnPurchOrder.md).

</td></tr><tr><td>

Received

</td><td>

The date and time at which the purchase order line item status was changed to **Received**.

</td></tr><tr><td>

Purchase order

</td><td>

The purchase order record number associated with this purchase order line item.

</td></tr><tr><td>

Rights per license pack

</td><td>

Rights associated with each pack that is purchased for Microsoft Per Core or Microsoft Per Core with CAL licenses.

</td></tr><tr><td>

Number of packs

</td><td>

Number of packs for Microsoft Per Core or Microsoft Per Core with CAL licenses.

</td></tr><tr><td>

Status

</td><td>

The current status of the purchase order line item: **Canceled**, **Ordered**, **Pending Delivery**, **Received**, or **Requested**.

</td></tr><tr><td>

Ordered quantity

</td><td>

The number of product models that were ordered.

</td></tr><tr><td>

Received quantity

</td><td>

The number of product models that were shipped and received. The vendor may have sent multiple shipments.The received quantity can be larger or smaller than the **Ordered** quantity. For example, you may have ordered five laptops but the vendor sent six.

</td></tr><tr><td>

Remaining quantity

</td><td>

The number of product models that still need to be received to fulfill the **Ordered** quantity.

</td></tr><tr><td>

List price

</td><td>

The price at which the item retails, not including discounts. If the system creates the purchase order from the service catalog ordering process, the purchase order line item inherits the list price from the associated vendor catalog item. If the vendor catalog item does not have a list price value and you have not entered a value, this field is automatically populated with the value from the **Cost** field.

</td></tr><tr><td>

Cost

</td><td>

The cost of a single product model, including discounts. If the system creates the purchase order from the service catalog ordering process, the purchase order line item inherits the cost from the associated vendor catalog item **Vendor Price**.

</td></tr><tr><td>

Total cost

</td><td>

The cost of a single product model multiplied by the value specified in **Quantity**.

</td></tr><tr><td>

Non-catalog request

</td><td>

Select this check box to create a requisition for an item that is not present in the product catalog of the organization.**Note:**

-   This field isn't visible on the form if you haven't published a procurement integration profile. For more information, see [Integrating with external procurement applications](../concept/integrate-ext-proc-ser.md).
-   If you select only a software model in the Product model field, this check box gets displayed on the form.
-   If you select an item in the Product Catalog field, the check box gets automatically unchecked.
-   If you haven't selected any item in the Product Catalog field, this check box is automatically checked, which indicates you are submitting a non-catalog request.


</td></tr><tr><td>

Stock Order

</td><td>

Read only and selected if the related request is using the bulk stock order workflow. **Note:** Appears for all purchase order line items when the Hardware Asset Management application is installed from ServiceNow Store.

</td></tr><tr><td>

Short description

</td><td>

A few words or short phrase describing the purchase order line item.

</td></tr></tbody>
</table>5.  Click **Submit**.

    The purchase order reopens with the line item listed. The purchase order and line item are in **Requested**s status.

6.  Continue adding purchase order line items for this vendor, as needed.

7.  After you initiate the order with the vendor and are ready to show that the order was placed, click **Order**.

    The status of the purchase order and line items change to **Ordered**.


**Parent Topic:**[Create a purchase order](t_CreateAPurchaseOrder.md)

**Related topics**  


[Vendor catalog items](../../product-catalog/concept/c_ManageVendorCatalogItems.md)

