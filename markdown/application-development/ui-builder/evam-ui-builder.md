---
title: Work with the Entity View Action Mapper for UI Builder
description: With UI Builder, you can use the Entity View Action Mapper \(EVAM\) application to standardize how the data sources in your components are displayed in your cards and lists.
locale: en-US
release: zurich
product: UI Builder
classification: ui-builder
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Dynamically expose data in UI Builder pages \(advanced feature\), Advanced UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Work with the Entity View Action Mapper for UI Builder

With UI Builder, you can use the Entity View Action Mapper \(EVAM\) application to standardize how the data sources in your components are displayed in your cards and lists.

## EVAM Overview

Entity View Action Mapper \(EVAM\) is an application that standardizes how different data sources are displayed in cards and lists. UI Builder uses EVAM data sources to show information in a component as a card grid view or as a list of information. You can add a toggle to your component to let users switch between card grid and list views.

EVAM consists of the following components:

-   Entity \(data source\). Associated data that you intend to display, such as a community post or a user.
-   View. How a card displays data and actions.
-   Actions. Action that it performs on the card. For example, you can activate a user into your system.
-   Map. A process that maps the data source to generic fields that are displayed on the card. You can also associate actions that trigger from the card view.

## EVAM and Multi-table data configuration

The EVAM is an option for users who understand and are comfortable working with JSON. The multi-table data configuration option is an alternative that gives you greater control over the presentation of data, makes it easier to configure the data, and enables you to remain in UI Builder. Use the option that you prefer. For more information, see [Multi-table data configuration](multi-source-data-configuration.md).

## EVAM data sources

You add EVAM data sources in UI Builder and bind them to a component.

![EVAM data resources in the select a data resource modal.](../image/evam-data-sources.png "EVAM data resources")

<table id="table_dz2_1g4_d4b"><thead><tr><th>

EVAM data source

</th><th>

Description

</th></tr></thead><tbody><tr><td>

EVAM Data Resource

</td><td>

Add an EVAM definition and other information about the data source. -   Type: Composite.
-   When to evaluate: In the **When to evaluate this data resource**, select **Immediately** to have the EVAM data resource instance evaluated on page load or select **Only when invoked** to use an event handler to evaluate the EVAM data resource.
-   EVAM definition: In the **EVAM Definition** field, add the EVAM definition record that is associated with the data resource.
-   Page cursor: In the **Page Cursor** field, add a page cursor for the EVAM definition.
-   Page size: In the **Page Size** field, add a size for the EVAM pagination.
-   Page number: In the **Page Number** field, add the page number for the EVAM pagination.
-   EVAM Filter Preference: In the **EVAM Filter Preference** field, enter the sys\_ids for the EVAM data filter.

 To add an event handler for when that data fetch is initiated, succeeded, or failed, select **Events**.

 In the **Now Code Editor** section, which is next to the Configuration pane, preview the EVAM definition script.

 ![EVAM Data Resource Configuration.](../image/EVAM-Data-Resource-Sample.png "EVAM Data Resource configuration")

</td></tr><tr><td>

Fetch EVAM Data

</td><td>

To add an EVAM definition and other information about the data source, select **Configuration**. -   Type: GRAPHQL.
-   When to evaluate: To have the EVAM data resource instance evaluated on a page load, select **Immediately**. To use an event handler to evaluate the EVAM data resource, select **Only when invoked**.
-   EVAM definition: In the **EVAM Definition** field, enter the EVAM definition record that is associated with the data resource.
-   Page cursor: In the **Page Cursor** field, enter a page cursor for the EVAM definition.
-   Page size: In the **Page Size** field, enter a size for the EVAM pagination.
-   Page number: In the **Page Number** field, enter the page number for the EVAM pagination.
-   EVAM Filter Preference: In the **EVAM Filter Preference** field, enter the sys\_ids for the EVAM data filter.

 To add an event handler for when that data fetch is initiated, succeeded, or failed, select **Events**.

 Preview the EVAM definition script in the **Now Code Editor** to the right of the Configuration pane.

![Fetch EVAM Data source configuration.](../image/evam-fetch-data.png)

</td></tr><tr><td>

Fetch EVAM Metadata

</td><td>

To select when to evaluate the EVAM data resource and add an EVAM definition, select **Configuration**. -   Type: GRAPHQL.
-   When to evaluate: To have the EVAM data resource instance evaluated on a page load, select **Immediately**. To use an event handler to evaluate the EVAM data resource, select **Only when invoked**.
-   EVAM definition: In the **EVAM Definition** field, enter the EVAM definition record that is associated with the data resource.

 To add an event handler for when that data fetch is initiated, succeeded, or failed, select **Events**.

 Preview the EVAM definition script in the **Now Code Editor** to the right of the Configuration pane.

![Fetch EVAM Metadata configuration.](../image/evam-fetch-metadata.png)

</td></tr><tr><td>

Search EVAM Data Resource

</td><td>

To add an EVAM definition, and other information about the data source, select **Configuration**. -   Type: Composite.
-   When to evaluate: To have the EVAM data resource instance evaluated on a page load. select **Immediately**. To use an event handler to evaluate the EVAM data resource, select **Only when invoked**.
-   EVAM Config ID: In the **EVAM Config ID** field, add the **EVAM Config ID** that is associated with the data record.
-   Search Context Config ID: In the **Search Context Config ID** field, add the **Search Context Config ID** that you are searching for.
-   Search Term: In the **Search Term** field, add the search terms that you are searching for.
-   Facet Filters: In the **Facet filters** field, add any facet filters to help define your search.
-   Search Filters: In the **Search Filters** field, add any search filters to help define your search.
-   Disable Spell Checking: In the **Disable Spell Checking** field, select if you desire spell checking to be on or off during your search.
-   Pagination Token: In the **Pagination Token** field, enter a pagination token if needed.

 To add an event handler for when that data fetch is initiated, succeeded, or failed, select **Events**.

 Preview the EVAM definition script in the **Now Code Editor** to the right of the Configuration pane.

![Search EVAM Data resource configuration.](../image/evam-search-data-resource.png)

</td></tr></tbody>
</table>-   **[Add an Entity View Action Mapper data resource to a page](../task/evam-working.md)**  
Add an Entity View Action Mapper \(EVAM\) data resource to your page in UI Builder so that you can standardize how the data sources in your components are displayed in your cards and lists.

**Parent Topic:**[Dynamically expose data in UI Builder pages \(advanced feature\)](data-resources.md)

