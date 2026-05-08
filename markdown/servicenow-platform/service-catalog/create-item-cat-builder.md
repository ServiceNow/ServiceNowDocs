---
title: Create a catalog item using a template
description: Make an item available in service catalog for catalog item requests.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Creating or editing catalog item template, Catalog Builder, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a catalog item using a template

Make an item available in service catalog for catalog item requests.

## Before you begin

Role required: catalog\_builder\_editor, catalog\_admin, or admin

## About this task

You must create a catalog item using one of the available catalog item templates.

Demonstrates how business owners can create catalog items in Catalog Builder.

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Builder**.

2.  Select the **Dashboard** tab and click **Create a new catalog item**.

3.  Review the steps involved in the creation process and click **Continue**.

4.  Select a template from the list and click **Use this item template**.

    **Note:**

    -   After you select the template, the preview of this template is available.
    -   You can only view templates assigned to you.
    -   Based on the template configuration, during the item creation or editing, few attributes have pre-specified values, are not editable, have limited options to select, and are mandatory.
    -   When selecting a record submission table for record producers, you can only select tables in that scope.
5.  Select **Build on your own**.

    By default, the **Build with Now Assist** option is selected, enabling you to leverage automated assistance for catalog generation. Alternatively, you can choose to create the item manually from scratch if you prefer a hands-on approach.

6.  Select **Build**.

7.  Based on how each step is defined in the template, specify the required information.

<table id="table_z5l_ck2_g4b"><thead><tr><th>

Step

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Details

</td><td>

-   Basic info: Item name and short description.
-   Item details: Description of the item.


</td></tr><tr><td>

Destination

</td><td>

Destination table in which a record producer creates records. **Note:** This step is available when using a record producer template.

</td></tr><tr><td>

Location

</td><td>

Catalogs, categories, and topics that the item can belong to.

 You can only view the catalogs, categories, and topics specified in the template.

 Configure catalogs and categories to make the catalog item discoverable on the Service Portal.

 In the Topics card, select taxonomy and its associated topics for a catalog item to make the catalog item discoverable on the Employee Center.

</td></tr><tr><td>

Questions

</td><td>

Question sets \(variable sets\) or questions for the item. By default, the question sets included in the template are added and cannot be removed. Available question types are restricted to those specified in the template.

 From the **Insert new question** list, you can include additional question sets, questions, deactivated questions, single-column container, two-column container, and line break. For information on creating a question and supported question types, see [Create a question for a catalog item in Catalog Builder](create-question-cat-builder.md).

 You can also add dynamic form behavior for a question. For information on adding dynamic form behavior, see [Edit a question in Catalog Builder](edit-question-cat-builder.md).

 **Note:**

-   The questions within a question set cannot be edited. The question sets can be reordered by dragging and dropping them.
-   Question sets specified in the template cannot be removed, while the ones added by the user can be removed.
-   Removal of question sets simply removes the association with the item and does not delete the question set.
-   A single-column question set can be added to a single-column or a two-column container. Two-column question set cannot be added to a container.
-   The questions for a catalog item are available as options on which a condition can be applied for a step when you create service fulfillment steps for that catalog item.


</td></tr><tr><td>

UI Policy

</td><td>

Configure catalog UI policies with scripts and multiple catalog UI policy actions in Catalog Builder to facilitate the creation of complex catalog items.

</td></tr><tr><td>

Client Script

</td><td>

Use catalog client scripts to control the behavior of the catalog items after publishing them for catalog item requesters.

</td></tr><tr><td>

Settings

</td><td>

Settings to configure the catalog item behavior in portals, such as Employee Center and Service Portal based on the request method.

 For example, you can determine whether to display buttons or options for adding attachments, making them mandatory, or saving the draft of the items while requesting them.

 If you want more people to edit a catalog item, then you can use this field. You can provide a user criteria to this field, and a user who matches with this user criteria, would be able to edit the item.

**Note:** Only catalog admin or owner of the item can modify the value in the field.

</td></tr><tr><td>

Access

</td><td>

User criteria to specify users for whom the item is available or not available.**Note:** You can add up to a maximum of 50 user criteria.

</td></tr><tr><td>

Fulfilment

</td><td>

Flow or workflow that you want to associate with this item. It defines how this catalog item can be fulfilled.When a catalog item is associated with a Workflow Studio flow that supports service fulfillment steps, the catalog item owner creating the item can configure steps within the flow.

 By default, the Step based request fulfillment flow is available in the base system.

 For information about defining service fulfillment steps, see [Define a service fulfillment step](create-sf-step.md).

 For information about Workflow Studio flows, see Flows.

</td></tr><tr><td>

Review and submit

</td><td>

Review the item and submit it.

</td></tr></tbody>
</table>    **Note:** A dot beside the step name indicates it has a mandatory field.

8.  To save your changes in each step, click **Save**.

    All edits to the item attributes are automatically saved when you navigate to the next step.

9.  To preview a catalog item in Portal, Now Mobile, or a Virtual Agent conversation, click **Preview**.

    **Note:** When you preview an item, you can interact with it but not submit it.

    1.  To preview the item in Portal, select **Portal** for the **View within** field.

        **Note:** Portal preview is based on portal URL configured for the catalog builder.

    2.  To view an item representation in Now Mobile, select **Now Mobile** for the **View within** field.

    3.  To preview a catalog item in a Virtual Agent conversation, select **Virtual Agent** for the **View within** field.

        The Service Management Virtual Agent Topic Blocks plugin \(com.glideapp.cs.sm\_topic\_blocks\) and one of these plugins must be installed.

        -   Glide Virtual Agent \(com.glide.cs.chatbot\)
        -   Glide Virtual Agent Lite \(com.glide.cs.chatbot.lite\)
        A Virtual Agent conversation whose sys\_id is specified in the **glide.sc.builder.va\_preview\_topic\_id** property is opened. By default, the property has the sys\_id of the base system Catalog builder preview topic. For information about this topic, see [Catalog builder preview topic conversation](../concept/catalog-builder-preview-topic.md). If the base system topic is used, the following scenarios are possible:

        -   If the item is supported in the conversation mode, you can preview the item in the Virtual Agent conversation by answering the questions but cannot submit a request for the item. For information about when a catalog item is supported in the conversation mode, [Service Catalog topic blocks in Virtual Agent powered by NLU](../concept/request-topic-blocks-va.md).
        -   If the item is not supported in the conversation mode, a link is provided for the portal preview of the item.
        -   When the required plugins are not installed, an illustration displaying a sample conversational experience for the catalog item submission appears.
    4.  To open the preview in a new tab, click **Open preview in a new tab**.

        **Note:** When you make any changes to the item and save it, the preview is dynamically refreshed in the opened tab.

10. To delete an unpublished draft item, click **Delete**.

    **Note:** You cannot delete a published item but can make it inactive.

11. Click **Submit**.

    **Note:** Until you submit the item, it is in the Draft state and is not available in the catalog.


-   **[Define a service fulfillment step](create-sf-step.md)**  
Define how a catalog item request should be fulfilled by creating simple service fulfillment steps.
-   **[Catalog builder preview topic conversation](../concept/catalog-builder-preview-topic.md)**  
From the catalog builder, a user can preview a catalog item in a Virtual Agent conversation.

**Parent Topic:**[Creating or editing catalog item template](create-cat-item-template-cat-builder.md)

**Related topics**  


[Edit a question in Catalog Builder](edit-question-cat-builder.md)

