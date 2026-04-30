---
title: Add a standard catalog item
description: Add a standard catalog item to your application in App Engine Studio \(AES\) so users can submit requests for services and offerings.
locale: en-US
release: zurich
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Add an experience, Enhance your app, Build, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Add a standard catalog item

Add a standard catalog item to your application in App Engine Studio \(AES\) so users can submit requests for services and offerings.

## Before you begin

Role required: sn\_app\_eng\_studio.user, sn\_app\_eng\_studio.admin, or delegated\_developer. For more information, see [Delegate developers using AES](../concept/aes-app-dev-workflow.md).

## About this task

A standard catalog item displays a form that users can fill in to create requests, such as a form to request an item or service. Standard catalog items make use of the Request table and produce a request record. In addition, generated request items are linked with a workflow, a catalog task, and any related approvals. Using standard catalog items, users can add multiple items to a cart and generate a request for each requested item. Use a catalog item when you want the service catalog form to generate a request, complete with a workflow, approvals, tasks, etc. When you add a standard catalog item, you're creating a standard version of the catalog item, which you must then continue editing in Catalog Builder before it's ready to deploy.

**Note:** If you created an application using a template, a standard catalog item may already be added to your application.

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **App Engine Studio**.

2.  From the My Apps page, open your application.

3.  In your application, next to Experience, select **Add**.

4.  Select **Standard catalog item** and select **Begin**.

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name for the standard catalog item.|
    |Short description|Brief overview of the standard catalog item.|

6.  Select **Edit catalog item**.

7.  Specify the required information.

    After completing each step, select **Save**.

<table id="table_qjc_gsy_hrb"><thead><tr><th>

Step

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Details

</td><td>

-   Basic info: Standard catalog item name and short description.
-   Item details: Description of the standard catalog item.

**Note:** You can attach files such as graphics, images, videos, or a link to an external source of information.

</td></tr><tr><td>

Location

</td><td>

-   Catalogs: Name of the catalog the standard catalog item belongs in.
-   Categories: Available categories that can be linked with the standard catalog item.


</td></tr><tr><td>

Questions

</td><td>

Questions for the standard catalog item.From the **Insert new question** list, you can include additional question sets, questions, deactivated questions, single-column container, two-column container, and line break. For information on creating a question and supported question types, see [Create a question for a catalog item in Catalog Builder](https://www.servicenow.com/docs/access?context=create-question-cat-builder&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

 You can also add dynamic form behavior for a question. For information on adding dynamic form behavior, see [Edit a question in Catalog Builder](https://www.servicenow.com/docs/access?context=edit-question-cat-builder&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

 **Note:**

-   The questions within a question set can't be edited. The question sets can be reordered by dragging and dropping them.
-   Question sets specified in the template can't be removed, while the ones added by the user can be removed.
-   Removal of question sets simply removes the association with the item and doesn't delete the question set.
-   A single-column question set can be added to a single-column or a two-column container. A two-column question set can't be added to a container.


</td></tr><tr><td>

Settings

</td><td>

Configure the standard catalog item based on the request method. Request method:

-   Order: Use this method in scenarios, such as a corporate laptop request.
-   Request: Use this method in scenarios, such as a code access request.
-   Submit: Use this method in scenarios, such as a reset password request.
 Other options:

-   Hide 'Add to cart' button: Option to hide the **Add to Cart** button for the standard catalog item. This option is automatically selected if the **Request method** is **Request** or **Submit**.
-   Hide 'Add to wishlist' button: Option to hide the **Add to wishlist** button on standard catalog items.
-   Hide quantity selector: Option to hide the **Quantity** list on standard catalog items.
-   Hide delivery time: Option to hide the **Delivery time** field on the standard catalog items. This option is automatically selected if you set the **Request method** to **Submit**.
-   Hide attachment button: Option to hide the **Attachments** button on standard catalog items.
-   Make attachment mandatory: Option to make the **Attachment** field mandatory on standard catalog items.


</td></tr><tr><td>

Access

</td><td>

Specify the group or individual users for whom the standard catalog item is available or not available.

</td></tr><tr><td>

Fulfillment

</td><td>

Flow with which you can associate the standard catalog item. The flow defines the fulfillment process for the standard catalog item. For more information on flows, see [Flows](https://www.servicenow.com/docs/access?context=flows&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

</td></tr><tr><td>

Review and Submit

</td><td>

Review and submit the standard catalog item.

</td></tr></tbody>
</table>8.  To preview a catalog item in Portal or Now Mobile, select **Preview**.

    **Note:** When you preview an item, you can interact with it but not submit it.

    1.  To preview the item in the portal, select **Portal** for the **View within** field.

        **Note:** Portal preview is based on the portal URL configured for the Catalog Builder.

    2.  To view an item representation in Now Mobile, select **Now Mobile** for the **View within** field.

    3.  To open the preview in a new tab, select **Open preview in a new tab**.

        **Note:** When you change the item and save it, the preview is dynamically refreshed in the opened tab.

9.  Select **Submit**.


## What to do next

For the standard catalog item you want to edit, select the menu icon \(![Menu icon](../image/menu-icon-purple.png)\) and select **Edit**.

-   **[Sample standard catalog item](../concept/standard-catalog-item-examples.md)**  
A standard catalog item displays a form that users can fill in to create requests, such as a form to request an item or service. Standard catalog items make use of the Request table and produce a request record. In addition, generated request items are linked with a workflow, a catalog task, and any related approvals. Using standard catalog items, users can add multiple items to a cart and generate a request for each requested item. Use a catalog item when you want the service catalog form to generate a request, complete with a workflow, approvals, tasks, etc.

**Parent Topic:**[Add an application experience](../concept/add-experience.md)

