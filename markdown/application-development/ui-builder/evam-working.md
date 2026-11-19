---
title: Add an Entity View Action Mapper data resource to a page
description: Add an Entity View Action Mapper \(EVAM\) data resource to your page in UI Builder so that you can standardize how the data sources in your components are displayed in your cards and lists.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/ui-builder/evam-working.html
release: zurich
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Work with the Entity View Action Mapper for UI Builder, Dynamically expose data in UI Builder pages \(advanced feature\), Advanced UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Add an Entity View Action Mapper data resource to a page

Add an Entity View Action Mapper \(EVAM\) data resource to your page in UI Builder so that you can standardize how the data sources in your components are displayed in your cards and lists.

## Before you begin

Role required: ui\_builder\_admin

## Procedure

1.  Navigate to **All** &gt; **Now experience framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    See [Configure how users interact with your applications in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/work-experiences.md) for more information on creating experiences.

3.  Open or create a page.

    For more information, see [Manage UI Builder pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/work-pages.md).

4.  If you do not have any components on your page, add a **Data set** component to your page.

    For more information, see [Add and configure components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/add-components.md).

5.  In the **Data and scripts** panel, select the **+** icon and then select **Data resource**.

    \[Omitted image "data-resource-open.png"\] Alt text: Arrow pointing to Data resource option.

6.  Enter `evam` in the search field.

7.  Select the EVAM data resource that you want to add and repeat this step for all the EVAM data resources for your page.

    \[Omitted image "evam-data-sources.png"\] Alt text: EVAM data resources.

8.  Configure each EVAM data resource.

<table id="table_dz2_1g4_d4b"><thead><tr><th>

EVAM data source

</th><th>

Description

</th></tr></thead><tbody><tr><td>

EVAM Data Resource

</td><td>

Add an EVAM definition and other information about the data source. -   Type: Composite.
-   When to evaluate: In the When to evaluate this data resource list, select **Immediately** to have the EVAM data resource instance evaluated on page load or select **Only when invoked** to use an event handler to evaluate the EVAM data resource.
-   EVAM definition: In the **EVAM Definition** field, add the EVAM definition record that is associated with the data resource.
-   Page cursor: In the **Page Cursor** field, add a page cursor for the EVAM definition.
-   Page size: In the **Page Size** field, add a size for the EVAM pagination.
-   Page number: In the **Page Number** field, add the page number for the EVAM pagination.
-   EVAM Filter Preference: In the **EVAM Filter Preference** field, add the sys\_ids for the EVAM data filter.
 To add an event handler for when that data fetch is initiated, succeeded, or failed, select **Events**.

 In the [Now Code Editor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/ui-builder-glossary.md) section, which is next to the Configuration pane, preview the EVAM definition script.

 \[Omitted image "EVAM-Data-Resource-Sample.png"\] Alt text: EVAM Data Resource Configuration.

</td></tr><tr><td>

Fetch EVAM Data

</td><td>

To add an EVAM definition and other information about the data source, select **Configuration**. -   Type: GRAPHQL.
-   When to evaluate: To have the EVAM data resource instance evaluated on a page load, select **Immediately**. To use an event handler to evaluate the EVAM data resource, select **Only when invoked**.
-   EVAM definition: In the **EVAM Definition** field, add the EVAM definition record that is associated with the data resource.
-   Page cursor: In the **Page Cursor** field, add a page cursor for the EVAM definition.
-   Page size: In the **Page Size** field, add a size for the EVAM pagination.
-   Page number: In the **Page Number** field, add the page number for the EVAM pagination.
-   EVAM Filter Preference: In the **EVAM Filter Preference** field, add the sys\_ids for the EVAM data filter.
 To add an event handler for when that data fetch is initiated, succeeded, or failed, select **Events**.

 Preview the EVAM definition script in the **Now Code Editor** to the right of the Configuration pane.

\[Omitted image "evam-fetch-data.png"\] Alt text: Fetch EVAM Data source configuration.

</td></tr><tr><td>

Fetch EVAM Metadata

</td><td>

To select when to evaluate the EVAM data resource and add an EVAM definition, select **Configuration**. -   Type: GRAPHQL.
-   When to evaluate: To have the EVAM data resource instance evaluated on a page load, select **Immediately**. To use an event handler to evaluate the EVAM data resource, select **Only when invoked**.
-   EVAM definition: In the **EVAM Definition** field, add the EVAM definition record that is associated with the data resource.
 To add an event handler for when that data fetch is initiated, succeeded, or failed, select **Events**.

 Preview the EVAM definition script in the **Now Code Editor** to the right of the Configuration pane.

\[Omitted image "evam-fetch-metadata.png"\] Alt text: Fetch EVAM Metadata configuration.

</td></tr><tr><td>

Search EVAM Data Resource

</td><td>

To add an EVAM definition and other information about the data source, select **Configuration**. -   Type: Composite.
-   When to evaluate: To have the EVAM data resource instance evaluated on a page load, select **Immediately**. To use an event handler to evaluate the EVAM data resource, select **Only when invoked**.
-   EVAM Config ID: In the **EVAM Config ID** field, add the **EVAM Config ID** that is associated with the data record.
-   Search Context Config ID: In the **Search Context Config ID** field, add the Search Context Config ID that you are searching for.
-   Search Term: In the **Search Term** field, add the search terms that you are searching for
-   Facet Filters: In the **Facet filters** field, add any facet filters to help define your search.
-   Search Filters: In the **Search Filters** field, add any search filters to help define your search.
-   Disable Spell Checking: In the **Disable Spell Checking** field, select if you desire spell checking to be on or off during your search.
-   Pagination Token: In the **Pagination Token** field, add a pagination token if needed.
 To add an event handler for when that data fetch is initiated, succeeded, or failed, select **Events**.

 Preview the EVAM definition script in the **Now Code Editor** to the right of the Configuration pane.

\[Omitted image "evam-search-data-resource.png"\] Alt text: Search EVAM Data resource configuration.

</td></tr></tbody>
</table>9.  Configure your data set component:

    -   Bind an EVAM data resource to your component.
    -   Set the **Show grid/list** toggle to on to let users choose between the grid or list view of the EVAM information on the page.
    -   Set the other configuration settings for the cards on the page.
10. Select **Save**.

11. View and test your page by selecting the **Preview** button.

    \[Omitted image "EVAM-SampleFinishedState.png"\] Alt text: Finished state of EVAM.


**Parent Topic:**[Work with the Entity View Action Mapper for UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/evam-ui-builder.md)

