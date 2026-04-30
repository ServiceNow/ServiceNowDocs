---
title: Create new purchase order exception form
description: Use the Create new purchase order exception form to provide details about the exception that is being created from a universal request.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Purchase Order Management, Source-to-Pay Operations, Finance and Supply Chain]
---

# Create new purchase order exception form

Use the Create new purchase order exception form to provide details about the exception that is being created from a universal request.

<table id="table_jr4_ghz_3hc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Purchase Order Exception

</td></tr><tr><td>

Number

</td><td>

Unique purchase order exception ID. This field is auto-populated.

</td></tr><tr><td>

Exception type

</td><td>

Type of exception being created. The default value is Delivery plan change.

</td></tr><tr><td>

Opened

</td><td>

Date and time when this purchase order exception is created.

</td></tr><tr><td>

Priority

</td><td>

Urgency and business impact of a purchase order exception.

</td></tr><tr><td>

Opened by

</td><td>

User who created this purchase order exception.

</td></tr><tr><td>

State

</td><td>

Current state of this purchase order exception. The options are:-   New
-   In progress
-   Closed
-   Canceled
-   Resolved

</td></tr><tr><td>

Supplier

</td><td>

Name of the supplier.

</td></tr><tr><td>

Assigned to

</td><td>

Name of the buyer that the exception is assigned to.

</td></tr><tr><td>

Related PO

</td><td>

Purchase order to which exception is related.

</td></tr><tr><td>

ERP line number

</td><td>

Identifier assigned to each item being ordered within a single purchase order. This field is auto-populated.

</td></tr><tr><td>

Delivery location

</td><td>

Location where the product is to be delivered. This field is auto-populated when the purchase order line is selected.

</td></tr><tr><td>

Intake source

</td><td>

Source of supply for the materials.

</td></tr><tr><td>

Short description

</td><td>

Short description of the exception.

</td></tr><tr><td>

Description

</td><td>

Long description of the exception.

</td></tr><tr><td colspan="2">

Delivery plan change

</td></tr><tr><td>

Exception sub-type

</td><td>

Type of purchase order exceptions. Options are:

 -   **Revised single delivery**: When you select this option, the order is delivered as a single shipment but with quantity or delivery date changes or both. Enter the revised quantity or delivery date or both.
-   **Phased delivery**: When you select this option, the order is split in multiple shipments. Save and then select **Manage deliveries** to enter the split dates and quantity.
-   **Rejection**: When you select this option, the order can’t be delivered. Enter a reason in the **Rejection reason** field.

</td></tr><tr><td>

Requested delivery date

</td><td>

Date when the buyer is requesting the delivery. This field is auto-populated when the purchase order line is selected.

</td></tr><tr><td>

Purchased quantity

</td><td>

Quantity purchased by the buyer. This field is auto-populated when the purchase order line is selected.

</td></tr><tr><td>

Proposed delivery date

</td><td>

Revised delivery date.

</td></tr><tr><td>

Proposed delivery quantity

</td><td>

Revised delivery quantity.

</td></tr></tbody>
</table>**Parent Topic:**[Purchase Order Management reference](purchase-order-mgmt-reference.md)

**Related topics**  


[Purchase order exception form](purch-order-exception-form.md)

[Delivery plan change form](create-delivery-plan-change.md)

