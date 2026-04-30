---
title: Delegated request experience
description: You can request a catalog item on behalf of another user or multiple users using the Requested For variable.
locale: en-US
release: xanadu
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 8
breadcrumb: [Configuring Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Delegated request experience

You can request a catalog item on behalf of another user or multiple users using the Requested For variable.

Delegated request experience comprises of the following entities:

-   Requested For variable for a catalog item. For information about this variable, see [Requested for](../reference/requested-for.md).
-   Requested For field on a requested item \(RITM\)

    **Note:** The form views, list views, and email notifications are not updated to reflect the Requested For field on a RITM.


## Configuration options

The following configuration options are available:

-   Specify who you want to submit the request for using the Requested For variable. You can also map the Requested For variable to a field on the table for record producers.
-   If required, configure the **Requested For** field on the RITM form. This field automatically stores the value of the Requested For variable.
-   Allow delegated requests for a catalog item using its **Access Type** field, where you can specify if a request can be submitted for a user who does not have access to the catalog item.
-   Submit a single request for an item on behalf of multiple users in Service Portal

**Important:** If two-step checkout is enabled, the delegated request experience is not supported.

## Request Management

After you submit a catalog item request, the Requested For variable value is copied to the **Requested For** field of the RITM. In case this field is not available on the RITM form, you should configure it.

**Note:** After you submit a catalog item, the **Requested For** field value is not automatically updated when the Requested For variable is modified, and vice versa.

In Service Portal,

-   If RITMs have different Requested For users, the following information is displayed in the order status page.
    -   The **Requested For** column to display the RITM's Requested For user.
    -   When the user viewing the Order Status page is not the user who submitted the request, the **Requestor** information to display the request's Requested For user. This is also applicable in Now Mobile, when the user viewing the RITM is not the user who requested it.
-   If the RITM's Requested For user is different from the request's \(REQ\) Requested For user, My Requests menu displays the RITM records to the user who the RITM is being requested for. If the RITM Requested for is the same as the REQ requested for user, My Requests menu displays REQs.
-   When you create a bundle from the cart by adding a catalog item with a Requested For variable, the item preserves the variable value. When you later add it to the cart to request for another user, you should edit the Requested For variable value as required.

## Request experience for a record producer

After you submit a record producer, the Requested For variable value is copied to the target record's field based on the **Map To Field** configuration.

## Request experience for an order guide

This experience is supported in an order guide only if the following conditions are met:

-   Order guide has a Requested For variable
-   All items in the order guide have a Requested For variable

A catalog item is included in an order guide based on the Requested For user's access to a catalog item.

-   When the user has no access to the catalog item and its **Access Type** is set as `Restricted`, that item is not included in the order guide.
-   When the user has no access to the catalog item and its **Access Type** is set as `Delegated`, that item is included in the order guide.

The Requested For variable value from the **Describe Needs** section is always cascaded to the Requested For variable of catalog items in rule bases.

-   The cascading of the Requested For variable value depends just on the variable type, but not the variable name.
-   The Requested For variable value is cascaded even when the **Cascade Variables** check box is not selected for the order guide.
-   The Requested For variables in the included catalog item cannot be edited.

## Submitting a catalog item request for multiple users

To support submitting a request for multiple users, you can configure the Requested For variable of a catalog item.

1.  From the **Type Specifications** tab, select the **Enable also request for** check box.
2.  Specify the roles in the **Roles to use also request for** field that can submit a catalog item request for multiple users. If no role is specified, anyone who has access to the catalog item can submit the request.

After you configure the Requested For variable of a catalog item, the **Also request for** field is displayed for that item in Service Portal. After you specify multiple users in this field, you can:

-   Add the item to the cart
    -   Separate cart items are created for each user specified in the **Also request for** field.
    -   The Requested For variable of each cart item is populated with the corresponding user.
-   Submit the request
    -   A single request is created and assigned to the current logged-in user requesting the item
    -   Separate RITMs are created, one for each user specified in the **Enable also request for** field and the Requested For variable.

**Note:**

-   This experience is available in Service Portal.
-   This experience is not available in Now Mobile and Workspace.
-   This experience is not available for a record producer and order guide.
-   The **Also request for** field is not displayed in the wish list and cart.
-   Catalog client scripts, catalog UI policies, and g\_form\(\) APIs are not applicable for the **Also request for** field.
-   The **Also request for** field is displayed only if the Requested For variable is editable. For example, the field is not displayed if the requesting user has no write permissions for the Requested For variable, or if the variable is made read-only via catalog client scripts.
-   You can add up to a maximum of 50 users in the **Also request for** field.
-   If any of the users does not have access to a catalog item with **Access Level** set as **Restricted**, then the item cannot be added to cart.

## Request cloning

When you clone a request:

-   The Requested For value for the cloned request is updated with the user for whom the request is being cloned.
-   The Requested For value for cloned RITMs \(with or without a Requested For variable\) is updated with the user for whom the request is being cloned for the following entities:
    -   RITM Requested For user
    -   Requested For variable value

For information about cloning requests, see [Clone requests](../task/t_EnablingBulkRequests.md).

**Important:**

-   You can clone a request only when all RITMs are requested for the same user.
-   You cannot clone a request for a user who does not have access \(based on **Access Type**\) to any item in the request.
-   Variable dependencies on the Requested For variable are not considered when a request is cloned.

## Cart behavior

Using the Requested For variable, you can add multiple catalog items to the cart for different users and submit the cart as one request. When you submit a request for a cart with multiple items, a single request is created with separate RITMs, one for each catalog item. In this case, the **Requested for** field of each RITM inherits the corresponding Requested For variable value.

When you add multiple items to the cart for different users and submit the request, a single request is created with a separate RITM for each catalog item with the corresponding Requested For user.

<table id="table_vxg_q41_hmb"><thead><tr><th>

Scenario

</th><th>

Cart behavior

</th></tr></thead><tbody><tr><td>

All items in the cart have a Requested For variable and are requested for the same user

</td><td>

-   Requested For value of the RITM is the Requested For variable value.
-   Requested For value of the request is the Requested For variable value.

</td></tr><tr><td>

All items in the cart have a Requested For variable and are requested for different users

</td><td>

-   Requested For value of the RITM is the Requested For variable value.
-   Requested For value of the request is the logged-in user or the default Requested For user specified in the cart.

</td></tr><tr><td>

No items in the cart have a Requested For variable

</td><td>

-   Requested For value of the RITM is the default Requested For user specified in the cart.
-   Requested For value of the request is the logged-in user or the default Requested For user specified in the cart.

</td></tr><tr><td>

Few items in the cart have a Requested for Variable while others do not

</td><td>

-   Requested For value of the RITM is one of the following:
    -   If a Requested For variable exists, it is the variable value.
    -   If no Requested For variable value exists, it is the logged-in user or the default Requested For user specified in the cart
-   Requested For value of the request is the logged-in user or the default Requested For user specified in the cart.

</td></tr></tbody>
</table>## Passing parameters for the Requested For variable

You can use parameters in ServiceNow AI Platform and Service Portal to specify the default Requested For variable value for a catalog item.

-   In Platform, pass a user's sys\_id as the **sysparm\_requested\_for** value in the URL.
-   In Service Portal, specify the **requested\_for\_id** and **requested\_for\_display** parameters in widget instance options.

    For example, navigate to a catalog item widget, press Ctrl+click to select **Instance in Page Editor**, and specify the following parameters in the **Additional options, JSON format** field.

    ```
    "requested_for_id": "a8f98bb0eb32010045e1a5115206fe3a 
    "requested_for_display": "Abraham Lincoln"
    ```


**Note:** The Requested For value is set after the catalog form is loaded.

-   **[Configure the default behavior to request items for other users](../task/config-default-behavior-request-other-user.md)**  
Define the default behavior when no roles are specified in the **glide.sc.req\_for.roles** property.

**Parent Topic:**[Configuring Service Catalog](configuring-service-catalog.md)

**Related topics**  


[Types of service catalog variables](../reference/r_VariableTypes.md)

