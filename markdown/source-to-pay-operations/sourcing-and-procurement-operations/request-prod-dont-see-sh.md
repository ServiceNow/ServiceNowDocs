---
title: Request for products that you don't see on Shopping Hub
description: Place a request for one or more products that are currently not listed on the Shopping Hub portal. You can do this from Shopping Hub Home or directly from Employee Center.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Request for products or services that you don't see on ShoppingHub, Using Shopping Hub, Use, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Request for products that you don't see on Shopping Hub

Place a request for one or more products that are currently not listed on the Shopping Hub portal. You can do this from Shopping Hub Home or directly from Employee Center.

## Before you begin

Role required: sn\_shop.shopper

## Procedure

1.  Navigate to **All** &gt; **ShoppingHub** &gt; **ShoppingHub Home**.

2.  Select **Don't see what you need?**.

    ![Requesting for products that are currently not listed on the Shopping Hub.](../image/spo-request-for-products-not-on-sh.png)

    The Purchase requests page is displayed from the Employee Center catalogs.

    ![Purchase requests page from where you can raise a request for products that are not listed on Shopping Hub.](../image/spo-sh-purchase-requests.png)

    **Note:** To directly access from Employee Center, navigate to **Purchases and expenses** &gt; **Purchase requests**.

3.  Select **I need a product**.

4.  On the form, fill in the details of the products that you’re looking for.

    ![Filling the product details to create a sourcing request.](../image/spo-sh-need-a-product-form.png)

<table id="table_hjz_1fd_flb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Who is this request for?

</td><td>

Name of the employee, shopper, or business owner who needs this product.**Note:** If you’re logged in as a fulfiller, you can raise this request for a shopper as well. Also, shoppers can select their delegates here.

</td></tr><tr><td>

What project is this request for?

</td><td>

Project for which this request is being raised.**Note:** This field is available only when you have the Procurement with Project Management \(sn\_spend\_ppm\) application installed, and also have the IT Project User role. For more information, see [Sourcing and Procurement Operations integration with Project Management](../concept/integration-psm-ppm.md).

</td></tr><tr><td>

What do you need for this request?

</td><td>

Type of request. The options are:-   I need a quote
-   I need a proposal
-   I need a proof of concept
-   I need more information about the products or suppliers


</td></tr><tr><td>

What suppliers do you want to request from?

</td><td>

Details of the suppliers you want to request from. The options are:-   Existing suppliers in the system: Add one or many suppliers from the list of existing suppliers. If you’ve already contacted them, select the appropriate option, and enter details of the supplier contact such as first and last names, job title, and registered email ID.

**Note:** Before you save the supplier contact details, ensure that your admin has set up the email domains for the supplier contacts, and the corresponding records are available in the Supplier Email Domain table.

-   External suppliers: Add one or many suppliers, and enter details of the supplier contact such as first and last names, job title, and registered email ID.

**Note:** It is recommended that you search from the existing suppliers first, and if the supplier you’re looking for doesn’t exist, enter one you want to work with.

-   I don't have any suppliers in mind.
For more information on adding suppliers, see:

-   From Platform: [Add a supplier](create-supplier.md).
-   From the supplier catalog: [Add a supplier contact using the supplier catalog](../../supplier-lifecycle-operations/task/enroll-contact-catalog.md).
-   From Source-to-Pay Workspace: [Add a supplier contact from the Source-to-Pay Workspace](../../supplier-lifecycle-operations/task/add-supplier-contact.md).


</td></tr><tr><td>

Default delivery address

</td><td>

Address for delivery. The options are:-   A saved address: In this case, the primary saved address of the logged-in user is displayed.
-   A work address: In this case, you must select who is receiving the item, or the business owner.
-   Somewhere else


</td></tr><tr><td>

Default delivery date

</td><td>

Estimated date range for delivery. The options are:-   As soon as possible: For the quickest delivery slot possible for the product. This is calculated based on the product category of each selected product.
-   A specific date: If you have a specific date in mind for the delivery of the product.
-   I am not sure: A time frame for the delivery of the product.
**Note:** You can select a date or date range that is in the past, present, or future. If you select a date range, you must enter your requested start and end dates to proceed.

</td></tr><tr><td>

Add the products you’d like to request

</td><td>

Add one or more products that you’re looking for, along with details such as product category, name of the product, specific requirements, if any, link to an example of what you’re looking for, quantity or budget amount, currency, delivery address, delivery date, and so on.**Note:** Here, you have the option to select different delivery addresses and dates for the individual products, as required, or go with the same options from the parent purchase.

</td></tr><tr><td>

Why do you need these products?

</td><td>

Reason behind this product requirement.

</td></tr><tr><td>

Are there additional details or questions you'd like to include?

</td><td>

Additional details, if any.**Note:** You must answer this question if you have selected **I need more information about the products or suppliers** in the **What do you need for this request?** field.

</td></tr></tbody>
</table>5.  Select **Save as Draft** if you want to save a draft in your requests and plan to complete it later.

6.  Select **Submit**.

    Individual sourcing requests are created for each product that you’ve requested for, with individual lines for the selected suppliers.


## What to do next

View your sourcing request details from the **Requested items** tab, where a complete summary of your request lines is displayed. You can also view the details from the My Purchases page in Shopping Hub.

In case of errors, check your system logs to detect any issues with the record producer submission. ​However, if you were able to submit successfully, check your event logs to verify whether the asynchronous event sn\_shop.process\_non\_catalog\_sourcing was triggered to initiate creation of the sourcing requests.

**Parent Topic:**[Requesting for products or services that you don't see on ShoppingHub](../concept/request-prod-serv-dont-see-sh.md)

