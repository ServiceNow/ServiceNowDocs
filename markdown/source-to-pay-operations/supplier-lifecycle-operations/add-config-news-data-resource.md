---
title: Add and configure the Get News data resource in UI Builder
description: Add and configure the Get News - Composite data resource in UI Builder to dynamically retrieve supplier news in the News and Activity section of the Source-to-Pay Workspace.
locale: en-US
release: yokohama
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring a custom API to dynamically fetch supplier news, News Integration for Supplier Lifecycle Operations, Integrating Supplier Lifecycle Operations with other applications, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Add and configure the Get News data resource in UI Builder

Add and configure the Get News - Composite data resource in UI Builder to dynamically retrieve supplier news in the News and Activity section of the Source-to-Pay Workspace.

## Before you begin

Create a REST message for a custom API. For more information, see [Create a REST message for a custom API](create-custom-api-rest.md).

Role required: admin

## About this task

A data resource is the data that a page fetches to display the content in the components. For more information, see [Data resources in UI Builder](https://www.servicenow.com/docs/access?context=data-resources&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US) .

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  On the **Page Collections** tab, do one of the following:

    -   For Supplier Manager Workspace, select **SLM Record page tabs**.
    -   For Source-to-Pay Workspace, select **S2P SLM Record page tabs**.
3.  In the About section, select **About default**.

4.  From the lower-left pane, select the **+** icon next to the Data and scripts section.

5.  In the Select data or script to add panel, select **Data resource**.

6.  In the Select a data resource dialog box, in the search field, enter **Get News – Composite**.

    In the Select a data resource section, you can add and configure data resource instances for your page. If you have any inherited data resources, you see them listed in the Inherited data resource pane but they are read-only. You do not configure inherited data in UI Builder.

7.  Select the **Get News – Composite** tile and then select **Add** to add it to your page.

8.  Select the **Configure** tab and then do the following:

    1.  In the **When to evaluate this data resource** list, select when you want to evoke the data resource.
    2.  In the **News Api** list, select the name of the REST message record.
    3.  In the **News Api Method** list, select the name of the GET HTTP request method.
    4.  In the **Query Params** field, select **Edit**.

        The Query Params dialog box is displayed.

    5.  On the **Edit JSON** tab, enter the query parameters, and then select **Apply**.
    6.  In the **Response Base Path** field, enter the top-level object to retrieve information from.

        You can also specify nested objects.

    7.  In the **Response Field List** field, select **Edit**.

        The Response Field List dialog box is displayed.

    8.  On the **Edit JSON** tab, enter the fields that you want to display in the response, and then select **Apply**.
    **Note:** Specifying specific fields enables you to retrieve filtered responses for REST endpoints. The response includes only the requested fields and objects.

9.  Select **Save**.


**Parent Topic:**[Configuring a custom API to dynamically fetch supplier news](../concept/config-supplier-news-api.md)

**Previous topic:**[Create a REST message for a custom API](create-custom-api-rest.md)

**Next topic:**[Update the field names in the UX client script](update-client-script.md)

