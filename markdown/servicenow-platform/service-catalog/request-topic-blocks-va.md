---
title: Service Catalog topic blocks in Virtual Agent powered by NLU
description: You can design a topic conversation in the Virtual Agent powered by Natural Language Understanding \(NLU\) by including reusable topic blocks to perform request submission tasks.
locale: en-US
release: yokohama
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Catalog Conversational Coverage, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Service Catalog topic blocks in Virtual Agent powered by NLU

You can design a topic conversation in the Virtual Agent powered by Natural Language Understanding \(NLU\) by including reusable topic blocks to perform request submission tasks.

## Search Catalog Item

You can use this topic block to search for a catalog item based on the search criteria. If there are multiple search results, you can select one from a carousel view.

|Parameter|Description|
|---------|-----------|
|query\_term|Keyword to search for a catalog item. For information on configuring keyword search for a catalog item, see [Configure keyword search for catalog items](../task/search-catalog-item.md).|
|catalogs|Comma-separated list of catalogs where a catalog item should be searched for.|
|result\_limit|Number of search results that should be displayed. By default, this number is set to 5.|

<table id="table_pks_mg1_3mb"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

catalog\_item\_id

</td><td>

If a catalog item is selected, sys\_id of the item is returned. If no catalog item is selected, that is, **None of these** option is selected, -1 is returned.

</td></tr><tr><td>

item\_type

</td><td>

sys\_class\_name of the catalog item that the user selected.

</td></tr><tr><td>

is\_conversational

</td><td>

Specifies if the catalog item can be requested in the conversation mode in Virtual Agent.

</td></tr></tbody>
</table>## Request Catalog Item

You can use this topic block to request for a catalog item.

|Parameter|Description|
|---------|-----------|
|catalog\_item\_id|sys\_id of the catalog item that should be requested.|
|execute\_contextual\_search|Option to specify if the contextual search should be run for a record producer based on its configuration. For information on defining contextual search for a record producer, see [Define contextual search for record producer](https://www.servicenow.com/docs/access?context=t_CntxtSearchRP&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).|
|confirm\_catalog\_item|Option to specify whether the user must confirm the catalog item before continuing with the next step. If this is set to `false`, user can answer the catalog items questions by skipping the confirmation.|
|show\_end\_state\_card|Option to display the end state card information about the generated record to the user.|

<table id="table_gbq_4g1_3mb"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

record\_id

</td><td>

sys\_id of the record that is generated after the item submission.If the catalog item is not supported in the conversation mode or if the user does not have access to the item, -1 is returned.

</td></tr><tr><td>

record\_table

</td><td>

Name of the table in which the record is generated.

</td></tr><tr><td>

variables

</td><td>

Questions related to the catalog item.

</td></tr></tbody>
</table>## Virtual Agent render types

A catalog item can be rendered in Virtual Agent as a conversation, window, pop-up, or inline.

## Catalog item request using a conversation render type

A user can submit a request in the conversation mode \(by answering the questions in line\).

![Virtual Agent rendered as a conversation](../image/va-conversation-catalog.png)

The following conditions must be met when a user requests a catalog item in the conversation mode in Virtual Agent powered by NLU.

-   A catalog item cannot have more than the number of questions specified in the **glide.sc.conversational.request.question.limit** property. By default, this number is set to 10. For more information about this property, see [Service Catalog properties](../reference/r_ServiceCatalogProperties.md).
-   A catalog item can have non-scripted catalog UI policies. These UI policies should be defined such that variables are affected sequentially, that is, only a variable with the lower order affects a variable with the higher order.
-   A catalog item cannot have catalog client scripts that are defined for Now Mobile or Service Portal.
-   Only the following variables are supported:
    -   Attachment
    -   Check box \(A group of check box variables isn't supported\)
    -   Date
    -   Date/Time
    -   Email
    -   IP Address
    -   Label
    -   Lookup Multiple Choice \(without pricing implications and advanced reference qualifier\)
    -   Lookup Select Box \(without pricing implications and advanced reference qualifier\)
    -   Multiple Choice \(without pricing implications\)
    -   Multi Line Text
    -   Numeric Scale \(without pricing implications\)
    -   Reference \(without pricing implications and advanced reference qualifier\)

        **Note:** Reference type variables that correspond to a table that has more than 7000 records are not supported. The upper limit for the number of records can be specified in the **glide.sc.va.reference\_question\_choices.limit** property. By default, it is set to 7000.

    -   Requested For \(without pricing implications and advanced reference qualifier\)
    -   Rich Text Label
    -   Select Box \(without pricing implications\)
    -   Single Line Text
    -   URL
    -   Wide Single Line Text
    -   Yes / No
    -   Container variables
-   The following variable attributes are supported:

    -   ref\_ac\_order\_by
    -   allowed\_extensions
    -   max\_file\_size
    **Note:** All the other variable attributes are ignored in Virtual Agent.

-   A catalog item can have a single-row variable set but not a multi-row variable set.
-   If a catalog item has a default value configured for a question, the default value is displayed in Virtual Agent, which enables the user to proceed with the default value without having to select it manually. The user can also choose a different value other than the default value.
-   If a catalog item has a data lookup configured for a question, the setter value is displayed in Virtual Agent, which enables the user to proceed with the setter value or choose a different value. A catalog item with data lookup is not supported as a conversational item when the setter question precedes the matcher question.
-   User cannot skip the following type of questions for a catalog item:
    -   Lookup Multiple Choice
    -   Select Box
    -   Lookup Select Box
    -   Yes/No
    -   Numeric Scale \(If **Do not select first choice** configuration is not selected\)
    -   Multiple Choice \(If **Do not select first choice** configuration is not selected, or **Include none choice** configuration is selected\)
-   If the user is using Virtual Agent in a different supported collaboration tool like Microsoft Teams:
    -   Searching for a value using the search icon in choice type of fields is not supported.

        ![Searching for a choice field in Microsoft Teams](../image/msteams-choice.png "Choice type fields in Microsoft Teams")

        ![Searching for choice field in Virtual Agent](../image/va-choice.png "Choice type fields in Virtual Agent")

    -   Searching for a value in reference type of fields is performed in the form of a question.

        ![Searching for reference fields in Microsoft Teams](../image/msteams-reference.png "Reference type fields in Microsoft Teams")

        ![Searching for reference field in Virtual Agent](../image/va-reference.png "Reference type field in Virtual Agent")


If the catalog item is non-conversational, the request form can appear as any of these render types:

-   Inline
-   Pop-up
-   Window

The conditions determine whether the catalog item form for the non-conversational catalog item will appear as inline, pop-up, or window.

**Note:** Based on the number of questions, a **glide.sc.va.inline\_render.question.limit** property determines whether the catalog item form appears as inline or pop-up. By default, the property's value is 20.

<table id="table_nv2_hbj_dcc"><thead><tr><th>

The catalog item form appears as

</th><th>

Conditions

</th></tr></thead><tbody><tr><td>

Inline

</td><td>

-   The catalog item doesn’t contain custom or UI page variables.
-   If the catalog item contains 20 or fewer questions, the item form appears as inline. The default value of the **glide.sc.va.inline\_render.question.limit** property is 20.
-   The catalog item doesn’t contain multi-row variable set \(MRVS\).

</td></tr><tr><td>

Pop-up

</td><td>

-   The catalog item doesn’t contain custom or UI page variables.
-   If the catalog item contains more than 20 questions, the item form appears as a pop-up. The default value of the **glide.sc.va.inline\_render.question.limit** property is 20.

</td></tr><tr><td>

Window

</td><td>

-   The catalog item contains custom or UI page variables.
-   The **glide.sc.va.render\_type.legacy** property is set to true.

</td></tr></tbody>
</table>## Catalog item request using an inline render type

Catalog item requesters can submit a catalog item by filling the form inline in the Virtual Agent powered by NLU. While requesting a catalog item that’s marked with inline render type, the requester can fill the item and its options within the Virtual Agent conversation.

For example, a requester can fill a form inline in the Virtual Agent conversation and submit the item.

![Inline request of a catalog item](../image/inline-catalog-request-va.png "Inline request of a catalog item")

![Inline request of a catalog item](../image/inline-catalog-request-va-a.png "Inline request of a catalog item")

![Inline request of a catalog item](../image/inline-catalog-request-va-b.png "Inline request of a catalog item")

## Catalog item request using a pop-up render type

A user can submit a catalog item request as a pop-up for items, which are not conversational. In a pop-up, Virtual Agent provides a link for the user to submit the request in a pop-up without navigating to a new tab. A non-conversational catalog item can be rendered as a pop-up only if it does not have any Custom, Custom with label, or UI Page variables.

**Note:** If you do not want to render your Virtual Agent conversation as a pop-up, set the **glide.sc.va.render\_type.legacy** property to true, which renders all non-conversational catalog items in the configured portal in a new tab.

![Virtual Agent rendered as a popup](../image/va-popup-catalog.png)

## Catalog item request using a window render type

A user can submit a catalog item request in a window. In a window, Virtual Agent provides a link for the user to submit the request in the Service Portal defined in the **sn\_itsm\_va.com.snc.itsm.virtualagent.portal\_url** property. A non-conversational item is rendered as a window if it has a Custom, Custom with label, or UI Page variable.

A catalog item is rendered as a window if it is of the following types:

-   Content Item
-   Order Guide
-   Wizard Launcher
-   Standard Change Template

![Virtual Agent rendered as a window](../image/va-window-catalog.png)

-   **[Submit a request topic conversation](request-submission-va.md)**  
Users can submit a request in a Virtual Agent conversation.

**Parent Topic:**[Catalog Conversational Coverage](using-catalog-conversational-experience.md)

**Related topics**  


[Catalog builder preview topic conversation](catalog-builder-preview-topic.md)

