---
title: Add a record producer
description: A record producer enables users to create task-based records, such as an incident record, in apps you create in App Engine Studio \(AES\) without creating a request. It enables a better end-user experience by standardizing requests using a simplified form.
locale: en-US
release: australia
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Add an experience, Enhance your app, Build, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Add a record producer

A record producer enables users to create task-based records, such as an incident record, in apps you create in App Engine Studio \(AES\) without creating a request. It enables a better end-user experience by standardizing requests using a simplified form.

## Before you begin

Create a data table that the record producer will add a new record to when a user fills out the form. For more information, [Create a data model for your application](../concept/add-data.md).

Role required: sn\_app\_eng\_studio.user or delegated\_developer. For more information, see [Delegate developers using AES](../concept/aes-app-dev-workflow.md).

## About this task

A record producer is a simplified type of catalog item that displays a form for users to fill out. The completed and submitted form inserts a new data record in a selected custom target table that you set up. This type of catalog item enables users to create task-based records, such as an incident record \(without any of the more complex functionality that comes with using a standard catalog item, such as creating requests\). Use a record producer when you want the service catalog form to create a simplified type of record that isn't a request \(for example, a task record such as an incident, change, or enhancement, etc.\). When you add a record producer, you create a basic version of the record producer. You must then continue editing it in Catalog Builder before it's ready to deploy.

**Note:** If you created an application using a template, a record producer may already be added to your application.

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **App Engine Studio**.

2.  From the My Apps page, open your application.

3.  In your application, next to Experience, select **Add**.

4.  Select **Record Producer** and select **Begin**.

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name for the record producer.|
    |Short description|Brief overview of the record producer.|

6.  Select **Edit record producer**.

7.  In Catalog Builder, specify the required information.

    After completing each step, select **Save**.

<table id="id_s4j_c2f_5rb"><thead><tr><th>

Step

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Details

</td><td>

-   Basic info: Record producer name and short description.
-   Item details: Description of the record producer.

**Note:** You can attach files such as graphics, images, videos, or a link to an external source of information.

</td></tr><tr><td>

Destination

</td><td>

Table in which the record producer creates records.

</td></tr><tr><td>

Location

</td><td>

-   Catalogs: Name of the catalog the record producer belongs to.
-   Categories: Available categories that can be linked with the record producer.
-   Topics: Available topics that can be connected to the standard catalog item. Find out more about topics in Associate a catalog item with a taxonomy topic in Employee Center.


</td></tr><tr><td>

Questions

</td><td>

Questions for the record producer.From the **Insert new question** list, you can include additional question sets, questions, deactivated questions, single-column container, two-column container, and line break. For information on creating a question and supported question types, see Create a question for a catalog item in Catalog Builder.

 You can also add dynamic form behavior for a question. For information on adding dynamic form behavior, see Edit a question in Catalog Builder.

 **Note:**

-   The questions within a question set can't be edited. The question sets can be reordered by dragging and dropping them.
-   Question sets specified in the template can't be removed, while the ones added by the user can be removed.
-   Removal of question sets simply removes the association with the item and doesn't delete the question set.
-   A single-column question set can be added to a single-column or a two-column container. A two-column question set can't be added to a container.


</td></tr><tr><td>

Settings

</td><td>

Options to customize the record producer behavior.-   Hide 'Add to wishlist' button: Option to hide the **Add to wishlist** button for the record producer.
-   Hide attachment button: Option to hide the **Attachment** button for the record producer
-   Make attachment mandatory: Option to make the **Attachment** field required for the record producer.


</td></tr><tr><td>

Access

</td><td>

Group or individual users for whom the record producer is available or not available.

</td></tr><tr><td>

Review and Submit

</td><td>

Review and submit the record producer.

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

For the record producer you want to edit, select the menu icon \(![Menu icon](../image/menu-icon-purple.png)\) and select **Edit**.

-   **[Sample record producer](../concept/record-producers-example.md)**  
A record producer experience that you create in App Engine Studio \(AES\) is a service catalog form that generates a task record, such as an incident, instead of a request.

**Parent Topic:**[Add an application experience](../concept/add-experience.md)

