---
title: Request an order guide from Service Portal
description: Use the SC Order Guide widget on Service Portal to request an order guide with several catalog items for a specific purpose.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Service Catalog in Service Portal, Integrating Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Request an order guide from Service Portal

Use the SC Order Guide widget on Service Portal to request an order guide with several catalog items for a specific purpose.

## Before you begin

Role required: requester

Select the **Allow Cloning** instance option on the Order Status page to display the **Additional Actions** section after placing the request.

For information about the SC Order Guide widget, see SC Order Guide widget.

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Service Portal Home**.

    The Service Portal homepage is displayed.

2.  Select an order guide from Service Catalog.

3.  In the **Describe Needs** section, enter the required information and click **Next**.

    **Note:** The **Next** button is disabled until you fill all mandatory fields on the form.

4.  In the **Choose Options** section, enter the requirements for catalog items and click **Next**.

    **Note:**

    -   If a catalog item has fields that need user inputs, **Options** is displayed on the accordion.
    -   If the fields are mandatory, a red asterisk is displayed beside **Options**.
    -   The ordered quantity value is displayed in the **Quantity** field and can be modified only if the **Show quantity** option is selected while creating an order guide rule base,
    1.  To expand or collapse the catalog item information, click the accordion.

    2.  To include or exclude the catalog item from the order guide request, click the toggle on the accordion.

        **Note:** When the item is excluded from the order guide request, the item is not editable and the corresponding mandatory field restrictions are ignored.

    3.  To add an attachment for the catalog item, click the Add attachments icon \(![Icon to add attachments](../image/IconAddAttachmnt.png)\) and select the required attachment.

    4.  Click **Previous** to navigate to the **Describe Needs** section.

5.  In the **Summary** section, review the order guide summary.

6.  To add the order guide to the shopping cart, click the Add to Cart icon \(![Icon to add to cart](../image/IconAddTocart.png)\).

    **Note:** When you add an order guide to the cart, you can only edit the order guide instance in the cart.

7.  To go to the **Choose Options** section and edit the order guide items, click **Edit Options**.

8.  Click **Order Now**.

    The Order Confirmation window is displayed.

9.  From the **Request for** list, select the user for whom you are requesting.

    **Note:**

    -   By default, the user who is logged in is selected in this list.
    -   The User \[sys\_user\] table columns specified in the **Additional columns for the “request for” Service Catalog widget. Choose fields in the sys\_user table. Must be semicolon separated** \(**glide.sc.request\_for.columns**\) Service Catalog property are displayed in the **Request for** list and you can search for a user by the specified columns.
    -   You can provide additional widget options to control the **Request for** default value. For example:

        ```
        "requested_for_id": { 
        "value": "62826bf03710200044e0bfc8bcbe5df1" 
        }, 
        "requested_for_display": { 
        "value": "Abel Tuter" 
        }
        ```

10. If required, specify the **Delivery Information** and **Special instructions**.

11. To add one or more attachments for the order guide, click the add attachments icon \(![add attachment icon](../image/IconAddAttachmnt.png)\).

    You can browse and choose the files, drag the files, or copy and paste them in the Add attachments window.

12. Click **Checkout**.

    The corresponding request is displayed in the Order Status page with the request number, estimated delivery date for the entire order, price, and the order status of individual ordered items.

    **Note:**

    -   Use the instance options on the Order Status page to display the pre-defined columns.
    -   You can display either the RITM number or the name of the catalog item. By default, the name of the catalog item is displayed.
13. To clone a request for other users, perform the following steps.

    1.  In the **Additional Actions** section, from the **Also request for** list, select the required users and click **Submit**.

    2.  In the Cloning Requests window, click **Ok**.

        **Note:**

        -   The logged in user should be specified in the **List of roles \(comma-separated\) that can use bulk ordering functionality. Blank means all users** \(**glide.sc.allow.clone.roles**\)\) property.
        -   You can clone the request for multiple users.
        -   If a record producer is included in the order guide, a request is created for all items other than the record producer.
        -   When you clone a request that contains a multi-row variable set, the information that is specified in the multi-row variable set is available in all cloned requests. All UI policies and client scripts on the multi-row variable set are also cloned.
        -   A separate request is created for each specified user and that user is displayed in the **Requested For** field of the request.
        -   The **Opened By** field of the cloned requests is updated with the logged in user.
        -   A user can view the cloned request created for the user from the **Requests** menu option or the My Requests widget on the catalog homepage.

**Parent Topic:**[Service Catalog in Service Portal](../concept/catalog-on-portal.md)

**Related topics**  


[Access Service Catalog categories in Service Portal](access-categories-portal.md)

[Add an item to the wish list in Service Portal](add-to-wishlist-portal.md)

[Add a catalog item to the shopping cart](add-to-cart-portal.md)

[Request a catalog item from Service Portal](request-cat-item-portal.md)

[Request an order guide](t_OrderProcess.md#)

[Create an order guide](t_CreateAnOrderGuide.md)

