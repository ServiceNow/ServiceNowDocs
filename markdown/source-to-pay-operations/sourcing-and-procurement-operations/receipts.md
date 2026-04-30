---
title: Receipts
description: Receipts reference a purchase order line. Depending on the product type of the purchase, a goods receipt or services receipt is generated.
locale: en-US
release: xanadu
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Sourcing and Purchasing Automation, Exploring Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Receipts

Receipts reference a purchase order line. Depending on the product type of the purchase, a goods receipt or services receipt is generated.

If the product type of the purchase order is a good, then a goods receipt is generated. If the product type is services, then a services acknowledgment receipt is generated.

For a product of the type service, if the acknowledgment type is **Milestones**, then confirming a milestone also results in receipt generation. However, if the acknowledgment type is **Two way match**, receipt creation is disabled for this purchase order line.

Receipts can either be a partial or full receipt, and are used determine the status of the associated purchase order line and purchase order.

You can view all receipts from the **Receipt Acknowledgment** sub-module under the Sourcing and Purchasing Automation module. The following are the key fields of a receipt:

<table id="table_hmt_cwy_hlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

System-generated unique identifier of the receipt.

</td></tr><tr><td>

ERP number

</td><td>

ERP number generated for the receipt.

</td></tr><tr><td>

Received by

</td><td>

The recipient of the product.

</td></tr><tr><td>

Status

</td><td>

Status of the receipt.The status field is visible only when the ERP integration plugin is installed.

</td></tr><tr><td>

Supplier product

</td><td>

The product for which the receipt is generated.

</td></tr><tr><td>

Type

</td><td>

Type of the receipt based on the product type. For example, **Goods Receipt** or **Services Receipt**.

</td></tr><tr><td class="sub-head" colspan="2">

Summary Details

</td></tr><tr><td>

Purchase order line

</td><td>

The purchase order against which the receipt of the product is acknowledged.

</td></tr><tr><td>

Milestone

</td><td>

Milestone associated for this receipt. This field is visible only for a services receipt and if the acknowledgment type is milestones.

</td></tr><tr><td>

Quantity received

</td><td>

The quantity of the product received. This field is visible only for a good receipt.

</td></tr><tr><td>

Percentage received

</td><td>

Percentage of the service received.This field is visible only for a services receipt.

</td></tr><tr><td>

Amount received

</td><td>

Receipt amount for the service received.This field is visible only for a services receipt.

</td></tr></tbody>
</table>**Parent Topic:**[Sourcing and Purchasing Automation](purchase-experience-workflow.md)

