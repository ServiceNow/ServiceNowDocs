---
title: Edit a purchase order line
description: You can edit and revise the quantity of the product, budget, or delivery location of a purchase order line in a purchase order based on your requirements.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Purchase revision flows, Using Shopping Hub, Use, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Edit a purchase order line

You can edit and revise the quantity of the product, budget, or delivery location of a purchase order line in a purchase order based on your requirements.

## Before you begin

Role required: sn\_spend\_psd.requestor or shopper

## Procedure

1.  Navigate to **ShoppingHub Home** &gt; **My purchases**.

    Alternatively, you can edit a purchase from **Employee Center** &gt; **Purchase and Expense** &gt; **Purchase Requests** &gt; **Edit a purchase**. For more information, see [Edit a purchase line from a purchase requisition or order from Employee Center \(EC\)](edit-pur-req-emp-central.md).

2.  Select a purchase order and a purchase order line in it.

    **Note:** Remember that the **Edit** option isn’t available for purchases in the Close state.

3.  Select **Edit** on the purchase order line.

    You can also select the **More options** icon on the order line and select **Edit** to modify the details of the line.

    The **Edit a purchase** page displays the **Purchase summary** with the price and quantity information.

4.  On the form, fill in the fields:

    **Note:** If it's a product, you see Current delivery date and New delivery date fields. If it's a service, you see Current start date, New start date, Current end date, and New end date.

    For goods, you see the fields related to delivery dates, for service lines, you see the fields related to service dates.

<table id="table_gc2_kbk_qnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Current Quantity

</td><td>

Displays the existing or current numerical quantity of the product to purchase.The current quantity can be viewed but not edited.

</td></tr><tr><td>

New Quantity

</td><td>

Update the new numerical quantity of the product to purchase.You can view existing quantity by referring to the Current Quantity field.

</td></tr><tr><td>

Current delivery date

</td><td>

**Important:** This field is applicable only for products.

Displays the existing or current delivery date of the product.The current delivery date can be viewed but not edited.

</td></tr><tr><td>

New delivery date

</td><td>

**Important:** This field is applicable only for products.

Update the delivery date of the product according to your preference.

</td></tr><tr><td>

Current start date

</td><td>

**Important:** This field is applicable only for services.

Displays the current start date of the service.The current start date can be viewed but not edited.

</td></tr><tr><td>

New start date

</td><td>

**Important:** This field is applicable only for services.

Update the new start date of the service.

</td></tr><tr><td>

Current end date

</td><td>

**Important:** This field is applicable only for services.

Displays the current start date of the service.The current start date can be viewed but not edited.

</td></tr><tr><td>

New end date

</td><td>

**Important:** This field is applicable only for services.

Update the new end date of the service.

</td></tr><tr><td>

Where do you want this delivered?

</td><td>

The options are:-   To one of my saved locations
-   To an office location
-   To a new address
For example, you can select an office location.The delivery location available for selection is filtered based on the countries supplier can deliver to.

</td></tr><tr><td>

Would you like to edit something else?

</td><td>

-   Select **Yes** if you want to edit something on the purchase order.
-   Select **No** if you don't have anything to update on the purchase order.


</td></tr><tr><td>

Address

</td><td>

Select an address from the drop-down list.

</td></tr><tr><td>

Purchase Reason

</td><td>

Enter the reason for the purchase.

</td></tr></tbody>
</table>5.  In the Why are you editing this purchase? field, provide the reason for editing the request.

6.  Add an attachment to support your edit request, if applicable.

    This file is attached to the procurement case record initially. When the case is closed, the file is attached to the purchase order associated with that procurement case.

7.  Select **Submit Request**.


## Result

The step creates a procurement case with the details of the revised quantity, location, and other information. Associated request lines and tasks are created using this information.

## What to do next

-   Shoppers can review and edit the request details from **ShoppingHub** &gt; **My requests** or **My requests** from the footer.
-   Buyers can track the progress of the procurement case and procurement case line edit requests from **Source-to-Pay Workspace**.

**Parent Topic:**[Purchase revision flows](../concept/purchase-revision-flows.md)

**Related topics**  


[Purchase revision flows](../concept/purchase-revision-flows.md)

[Process Automation Designer flows for playbook](../concept/process-automation-designer-flows-psm.md)

