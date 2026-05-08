---
title: Define a search source
description: Configure a basic search source to query data from an instance table, or configure an advanced data fetch script to query data across multiple tables and data sources, or to pull data from anywhere on the web.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2026-05-08"
reading_time_minutes: 4
breadcrumb: [Zing search in Service Portal, Configuring search in a portal, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Define a search source

Configure a basic search source to query data from an instance table, or configure an advanced data fetch script to query data across multiple tables and data sources, or to pull data from anywhere on the web.

## Before you begin

Role required: admin

## Procedure

1.  In the platform UI, navigate to **Service Portal** &gt; **Portals** and select the portal you want to add search sources to.

2.  From the **Search Sources** related list, click **New** to add a search source.

3.  Define the fields on the **Search Source** form.

<table id="table_zxx_n3b_qz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The display value for the search category.

</td></tr><tr><td>

ID

</td><td>

The record ID. The value should be unique, and should not include any spaces or special characters.

</td></tr><tr><td>

Application

</td><td>

The scope of the search source.

</td></tr><tr><td>

Roles

</td><td>

If the Service Portal User Criteria Support plugin is not enabled, define user roles to access this search source.

</td></tr><tr><td>

Search page template

</td><td>

The HTML template that displays the search results. If defining a basic search source, you do not need to change the default template.

 For an example of a modified template, see [Tutorial: set up an external knowledge base search source](search-sp-advanced-ext-kb.md).

</td></tr></tbody>
</table>4.  Complete the fields on the **Data Source** tab.

<table id="table_fl5_dc5_nx"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Is scripted source

</td><td>

Adds an advanced data fetch script. If configuring an instance table as the data source, do not check this option.

</td></tr><tr><td>

Data fetch script

</td><td>

Script defining the endpoint and API calls to fetch data. This field is only visible when **Is scripted source** is selected.

 For an example of a data fetch script, see [Tutorial: set up an external knowledge base search source](search-sp-advanced-ext-kb.md).

 **Note:** If defining a facet generation script, inject the facets object into the data fetch script and update the script to generate data for each facet item. For an example, see the Knowledge Base and Service Catalog search sources. Search facets may not behave as expected if integrated into an advanced search source that queries data from a non- ServiceNow site.

</td></tr><tr><td>

Facet generation script

</td><td>

Script defining search facets for a scripted search source. Enable your end users to filter search results for a more meaningful result set. This field is only visible when **Is scripted source** is selected.

 **Note:** If defining a facet generation script, inject the facets object into the data fetch script and update the script to generate data for each facet item. For an example, see the Knowledge Base and Service Catalog search sources. Search facets may not behave as expected if integrated into an advanced search source that queries data from a non- ServiceNow site.

</td></tr><tr><td>

Table

</td><td>

Select a table from the list that you want to draw your results from. You can select any table in the platform. For example, User \[sys\_user\] or Knowledge \[kb\_knowledge\]. **Note:** Only indexed tables return search results. Learn more: Configure a table for indexing and searching.

</td></tr><tr><td>

Conditions

</td><td>

Filters results based on defined conditions. For example, Active is True.

</td></tr><tr><td>

Primary display field

</td><td>

Select which field you want to display on the search results page. For example, Name.

</td></tr><tr><td>

Display fields

</td><td>

Select additional fields to display on the search results page. For example, User ID, Email, and City.

</td></tr><tr><td>

Paginate results

</td><td>

Paginates search results. True by default.

 If **Is scripted source** is selected, the value updates to false. To enable pagination for a scripted search source, see [Paginate search source results](paginate-scripted-search-source.md).

 Define the maximum number of results per query for the search source in the Search Page widget or Faceted Search widget instance options.

</td></tr></tbody>
</table>5.  Configure **Typeahead** settings to allow search results to populate the search field based on user input.

    |Field|Description|
    |-----|-----------|
    |Enable typeahead|Allows typeahead functionality. If you do not want to integrate typeahead into your search source, clear the check box.|
    |Advanced typeahead config|Optionally add an advanced typeahead script to configure the way search results display. For more information, see [Create an advanced typeahead template](advanced-typeahead.md).|
    |Typeahead glyph|Adds an icon beside each typeahead result.|
    |Page|Defines a service portal page to display the selected result. For example, if **form** is configured, a selected typeahead result opens in a form.|

    ![Example Typeahead tab settings. Page field is set to form.](../image/basic-typeahead.png)

6.  Click **Submit**.


## What to do next

To enable end users to refine search results, [Add facets to a simple search source](create-search-filter.md).

-   **[Paginate search source results](paginate-scripted-search-source.md)**  
Limit the number of results that a search source displays at one time to improve performance. End users can load more results as needed.
-   **[Create an advanced typeahead template](advanced-typeahead.md)**  
Configure the way typeahead results display with an advanced template.
-   **[Tutorial: set up an external knowledge base search source](search-sp-advanced-ext-kb.md)**  
Define an advanced search source to return data from any source on the Internet. To understand the power of search sources, follow this tutorial to set up an external knowledge base search source.
-   **[Example: set up a GitHub search source](search-sp-advanced.md)**  
Set up an advanced search source that queries data from an external website.

**Parent Topic:**[Zing search in Service Portal](../concept/zing-search-service-portal.md)

