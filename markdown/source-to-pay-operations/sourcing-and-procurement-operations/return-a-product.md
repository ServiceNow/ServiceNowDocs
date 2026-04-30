---
title: Return a product
description: You can request a return for a product that has been fully or partially delivered to you.
locale: en-US
release: yokohama
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Using Shopping Hub, Using Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Return a product

You can request a return for a product that has been fully or partially delivered to you.

## Before you begin

Role required: sn\_spend\_psd.requestor or shopper

## About this task

You can raise a return request for multiple products belonging to the same purchase order or purchase requisition that has been fully or partially delivered to you.

## Procedure

1.  Navigate to **ShoppingHub Home** &gt; **My purchases**.

    Alternatively, you can return a purchase from **Employee Center** &gt; **Purchase and Expense** &gt; **Purchase Requests** &gt; **Return a purchase**.

2.  Select a purchase requisition, purchase order, or purchase line that has been delivered or partially delivered.

3.  Select **Return** from the **More options** or **Edit** menu, as applicable.

4.  On the form, fill in the fields:

<table id="table_gc2_kbk_qnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Return type

</td><td>

Type of return you want to request. The options are:-   **Return for a refund**
-   **Return for a replacement**


</td></tr><tr><td>

Business owner

</td><td>

Name of the business owner. This field is auto-populated.

</td></tr><tr><td>

Return scope

</td><td>

Select whether you want to return teh entire purchase or individual items from the purchase. The options are:-   **Entire purchase**
-   **Individual items**


</td></tr><tr><td>

Purchase order lines

</td><td>

This section is displayed if you select **Individual items** from the **Return scope** field.-   **Purchase order line**: Purchase order line that you want to modify.
-   **Product name**: Product associated with the purchase order lines.
-   **Quantity received**: Quantity of items that you have received.
-   **Quantity returned**: Quantity of items already returned before, if any, is auto-populated.
-   **Quantity to be returned**: Quantity of items to return. This field is displayed only if you selected **Return for a refund** in the **Return type** field.
-   **Quantity to be replaced**: Quantity of items to replace. This field is displayed only if you selected **Return for a replacement** in the **Return type** field.


</td></tr><tr><td>

How many would you like to return?

</td><td>

Quantity of items to return. Remember that the quantity must always be lesser than or equal to the delivered quantity.**Note:** This field is displayed only for line-level returns.

</td></tr><tr><td>

Reason for return

</td><td>

Reason for returning this purchase.

</td></tr></tbody>
</table>    **Note:** You can introduce new question variables to the form and enable additional validations, if required, from the respective record producer record.

5.  Select **Submit Request**.

    A confirmation message screen appears.


## Result

Depending on the type of return request, this procedure creates a procurement case of type Return a purchase or Replace a purchase, with the relevant details. Associated request lines and tasks are created using this information.

The fulfiller can approve or reject the return or replacement request. For more information, see the following topics:

-   [Process a return request in playbook](playbook-return-request.md)
-   [Process a replacement request in playbook](playbook-replacement-request.md)

## What to do next

-   Shoppers can review the request details from **Employee Center** &gt; **My Requests**.
-   Shoppers can review the request details from **ShoppingHub** &gt; **** &gt; **My purchases**, accessed from the profile image or from the footer.
-   Buyers can track the progress of the procurement case and procurement case line requests from **Source-to-Pay Workspace**.

**Parent Topic:**[Using Shopping Hub](../reference/use-shoppinghub-portal.md)

