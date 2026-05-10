---
title: Request a catalog item from Service Portal
description: Use the SC Catalog Item widget in Service Portal to request a catalog item.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Service Catalog in Service Portal, Integrating Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Request a catalog item from Service Portal

Use the SC Catalog Item widget in Service Portal to request a catalog item.

## Before you begin

Role required: requester

Select the **Allow Cloning** instance option on the Order Status page to display the **Additional Actions** section after placing the request.

For information about the SC Catalog Item widget, see [SC Catalog Item widget](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/sc-catalog-item-widget.md)

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Service Portal Home**.

    The Service Portal homepage is displayed.

2.  Select a catalog item or record producer from Service Catalog.

3.  Enter the required information in the catalog item form.

4.  Enter the number of items in the **Quantity** field.

5.  If required, perform any of these actions.

<table id="choicetable_sly_jsd_5bb"><tbody><tr><td id="d639486e136">

**Add attachments**

</td><td>

To add one or more attachments to the catalog item, select the choose a file link to browse and choose the files or directly drag the files in the **Add attachments** window.

</td></tr><tr><td id="d639486e151">

**Add to Cart**

</td><td>

To add the catalog item to the shopping cart, click the Add to Cart icon \(![Icon to add to the cart](../image/IconAddTocart.png)\).

</td></tr><tr><td id="d639486e166">

**Add to Wish List**

</td><td>

To add the catalog item to the wish list, click the Add to Wish List icon \(![Icon to add to the wishlist](../image/SPWishList.png)\).

</td></tr></tbody>
</table>6.  Click **Order Now**.

    The Order Confirmation window is displayed.

    **Note:** For a record producer, you can edit the label of the **Submit** button by using the widget instance options.

    For example, if you want to change the label to **Request**, press Ctrl+click on the catalog item widget, select **Instance in Page Editor**, and specify the following parameters in the **Additional options, JSON format** field.

    ```
    "record_producer_label":{
    			"value" : "Request"
    		}
    ```

7.  From the **Request for** list, select the user for whom you are requesting.

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

8.  If required, specify the **Delivery Information** and **Special instructions**.

9.  Click **Checkout**.

    The corresponding request is displayed in the Order Status page with the request number, estimated delivery date for the order, price, and the order status.

    **Note:**

    -   Use the instance options on the Order Status page to display the pre-defined columns.
    -   You can display either the RITM number or the name of the catalog item. By default, the name of the catalog item is displayed.
    -   When a service catalog item is ordered from an existing record, a link is added between the order item request and the parent record.
10. To clone a request for other users, perform the following steps.

    1.  In the **Additional Actions** section, from the **Also request for** list, select the required users and click **Submit**.

    2.  In the Cloning Requests window, click **Ok**.

        **Note:**

        -   The logged in user should be specified in the **List of roles \(comma-separated\) that can use bulk ordering functionality. Blank means all users** \(**glide.sc.allow.clone.roles**\) property.
        -   You can clone the request for multiple users.
        -   When you clone a request that contains a multi-row variable set, the information that is specified in the multi-row variable set is available in all cloned requests. All UI policies and client scripts on the multi-row variable set are also cloned.
        -   A separate request is created for each specified user and that user is displayed in the **Requested For** field of the request.
        -   The **Opened By** field of the cloned requests is updated with the logged in user.
        -   Select the **Requests** menu option or the My Requests widget on the catalog homepage to view the cloned request created for the user.

**Parent Topic:**[Service Catalog in Service Portal](../concept/catalog-on-portal.md)

**Related topics**  


[Access Service Catalog categories in Service Portal](access-categories-portal.md)

[Add an item to the wish list in Service Portal](add-to-wishlist-portal.md)

[Add a catalog item to the shopping cart](add-to-cart-portal.md)

[Request an order guide from Service Portal](request-order-guide-portal.md)

[Service Catalog request screens](../concept/c_RequestingAServiceCatalogItem.md#)

[Create a variable set and add it to an item](t_CreateAVariableSet.md#)

