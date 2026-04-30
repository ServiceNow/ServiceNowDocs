---
title: Edit a purchase requisition line
description: You can edit and revise the quantity of the product, budget, or delivery location of a purchase requisition line in a purchase requisition based on your requirements.
locale: en-US
release: xanadu
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Purchase revision flows, Using Shopping Hub, Using Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Edit a purchase requisition line

You can edit and revise the quantity of the product, budget, or delivery location of a purchase requisition line in a purchase requisition based on your requirements.

## Before you begin

Role required: sn\_spend\_psd.requestor or shopper

## Procedure

1.  Navigate to **ShoppingHub Home** &gt; **My purchases**.

    Alternatively, you can edit a purchase from **Employee Center** &gt; **Purchase and Expense** &gt; **Purchase Requests** &gt; **Edit a purchase**. For more information, see [Edit a purchase line from a purchase requisition or order using Employee Central \(EC\)](edit-pur-req-emp-central.md).

2.  Select a purchase requisition and a purchase requisition line in it.

    **Note:** Remember that the **Edit** option is not available for purchases in the Closed state.

3.  Select **Edit** on the purchase requisition line.

    You can also select the **More options** icon on the requisition line and select **Edit** to modify the details of the line.

    The **Edit a purchase** page displays the **Purchase summary** with the price and quantity information.

4.  On the form, edit the fields:

    **Note:** If it's a product, you will see Current delivery date and New delivery date fields, and if it's a service, you will see Current start date, New start date, Current end date, and New end date.

    For goods, we will show the fields related to delivery dates, for service lines, we show the fields related to service dates.

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

Select an address from the dropdown list.

</td></tr><tr><td>

Purchase Reason

</td><td>

Enter the reason for the purchase.

</td></tr></tbody>
</table>5.  In the Why are you editing this purchase? field, provide the reason for editing the request.

6.  Add an attachment to support your edit request, if applicable.

    This file is attached to the procurement case record initially, and then to the purchase requisition associated to that procurement case when the case is closed.

7.  Select **Submit Request** to complete the edit request.


## Result

The step creates a procurement case with the details of the revised quantity, location, and other information. Associated request lines and tasks are created using this information.

## What to do next

-   Shoppers can review and edit the request details from **ShoppingHub** &gt; **My requests** or **My requests** from the footer.
-   Buyers can track the progress of the procurement case and procurement case line edit requests from **Procurement Workspace**.

**Parent Topic:**[Purchase revision flows](../concept/purchase-revision-flows.md)

**Related topics**  


[Purchase revision flows](../concept/purchase-revision-flows.md)

[Process Automation Designer flows for playbook](../concept/process-automation-designer-flows-psm.md)

