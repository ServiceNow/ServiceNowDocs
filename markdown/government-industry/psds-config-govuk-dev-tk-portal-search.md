---
title: Configure GDS Service Portal Search Widgets
description: Configure and use search widgets for GDS Service Portal so that portal users can take advantage of intelligent query features and find the answers they need.Configure the ServiceNow AI Search application for GDS Service Portal so that portal users can take advantage of intelligent query features and find the answers they need.Configure the ServiceNow AI Search application for GDS Service Portal so that portal users can take advantage of intelligent query features and find the answers they need.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/psds-config-govuk-dev-tk-portal-search.html
release: australia
topic_type: concept
last_updated: "2026-06-02"
reading_time_minutes: 7
breadcrumb: [Configure UK GDS Service Portal, GOV.UK Developer Toolkit, Set up self-service, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure GDS Service Portal Search Widgets

Configure and use search widgets for GDS Service Portal so that portal users can take advantage of intelligent query features and find the answers they need.

GDS Service Portal displays search results data within a widget on the search page. Search data displays within a widget on the search page.

To make data searchable from the GDS Service Portal portal, create a search source that fetches that data from a single table within your instance, from multiple tables, or from an external site.

You can also configure **Typeahead** search settings to allow search results to populate the search field based on user input.

Enable AI Search to take advantage of intelligent query features and allow constituents to find the answers they need.

**Parent Topic:**[Configure the GOV.UK Design System \(GDS\) Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-config-gds-content-pack-gsp.md)

## Configure search sources in GDS Service Portal

Configure the ServiceNow AI Search application for GDS Service Portal so that portal users can take advantage of intelligent query features and find the answers they need.

### Before you begin

Role required: admin or sp\_admin

**Note:** Verify that the scope is set to GOV.UK Developer Toolkit.

### About this task

A search source is a record that describes the behavior and source of searchable data. A search source defines:

-   Where to retrieve search data from.
-   Whether search suggestions can populate the search field based on user input.
-   How a search entry displays in the search result page.

Search sources have basic and advanced configurations. A basic search source configuration allows you to define a table or other source \(such as a knowledge base\) within your instance as a source of searchable data for the search source to query and return results from. An advanced configuration uses a data fetch script that will fetch data from multiple tables or from any number of sources on the web, and return a data result array to the search widget. For information on how to configure an advanced search source that pulls data from external tables or sources, see [Tutorial: set up an external knowledge base search source](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/search-sp-advanced-ext-kb.md).

By default, the GDS Service Portal has the following search sources configured. This means that when a constituent searches for something using the search widget on the portal, the widget will display results from these three sources, with an option to filter by source.

-   Knowledge Base \[uk-gds-kb\], for which the search results display a list of knowledge articles related to the search.
-   Services \[uk-gds-service-catalog\], for which the search results display a list of available services that match or partially match the search query
-   Government Cases \[gds-cases\], for which the search results display a list of cases related to the search query from the Government Service Case table \[sn\_gsm\_government\_service\_case\] that the user has access to.

To configure a basic search source to query data from a source other than the default \(another knowledge base, catalog, table, or other source that is already created within your instance\), do the following.

### Procedure

1.  In the platform UI, navigate to **Service Portal** &gt; **Portals** and select the portal you want to add search sources to.

2.  From the **Search Sources** related list, select **New** to add a search source.

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

The scope of the search source. By default, this field will display GOV.UK Developer Toolkit and cannot be edited.

</td></tr><tr><td>

Roles

</td><td>

Define user roles to access this search source. Select the pencil icon \(\[Omitted image "pencil-outline-24.svg"\]\) to configure user roles.

</td></tr><tr><td>

Search page template

</td><td>

The HTML template that displays the search results. If defining a basic search source, you don't need to change the default template. For an example of a modified template, see [Tutorial: set up an external knowledge base search source](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/search-sp-advanced-ext-kb.md).

</td></tr></tbody>
</table>4.  Complete the fields on the **Data Source** tab.

<table id="table_fl5_dc5_nx"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Is scripted source

</td><td>

Adds an advanced data fetch script. If configuring an instance table or knowledge base as the data source \(basic configuration\), do not select the checkbox for this option.

</td></tr><tr><td>

Data fetch script

</td><td>

Script defining the endpoint and API calls to fetch data. This field is only visible when **Is scripted source** is selected.

 For an example of a data fetch script, see [Tutorial: set up an external knowledge base search source](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/search-sp-advanced-ext-kb.md).

 **Note:** If defining a facet generation script, inject the facets object into the data fetch script and update the script to generate data for each facet item. For an example, see the Knowledge Base and Service Catalog search sources. Search facets may not behave as expected if integrated into an advanced search source that queries data from a non- ServiceNow site.

</td></tr><tr><td>

Facet generation script

</td><td>

Script defining search facets for a scripted search source. Enable your end users to filter search results for a more meaningful result set. This field is only visible when **Is scripted source** is selected.

 **Note:** If defining a facet generation script, inject the facets object into the data fetch script and update the script to generate data for each facet item. For an example, see the Knowledge Base and Service Catalog search sources. Search facets may not behave as expected if integrated into an advanced search source that queries data from a non- ServiceNow site.

</td></tr><tr><td>

Table

</td><td>

Select a table from the list that you want to draw your results from. You can select any table in the platform.**Note:** Only indexed tables return search results. Learn more: [Configure a table for indexing and searching](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/configure-single-table-for-indexing.md).

</td></tr><tr><td>

Conditions

</td><td>

Filters results based on defined conditions. For example, Active is True. This field is optional.

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

 If Is scripted source is selected, the value updates to false.

 Define the maximum number of results per query for the search source in the Search Page widget or Faceted Search widget instance options.

</td></tr></tbody>
</table>5.  Configure **Typeahead** settings to allow search results to populate the search field based on user input.

    |Field|Description|
    |-----|-----------|
    |Enable typeahead|Allows typeahead functionality. If you don't want to integrate typeahead into your search source, unselect the check box.|
    |Advanced typeahead config|Optionally add an advanced typeahead script to configure the way search results display. For more information, see [Create an advanced typeahead template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/advanced-typeahead.md).|
    |Typeahead glyph|Adds an icon beside each typeahead result.|
    |Page|Defines the service portal page on which the selected results will be displayed. For example, if **form** is configured, a selected typeahead result opens in a form. If **uk\_gds\_case\_details**is configured, a selected typeahead result opens on the case details page.|

    \[Omitted image "image.basic-typeahead"\] Alt text: Example Typeahead tab settings. Page field is set to form.

6.  Select **Submit**.


### Result

Search capabilities are enabled throughout the portal, and constituents can use search to see results from various sections of the portal the next time they log in.

## Enable AI Search in GDS Service Portal

Configure the ServiceNow AI Search application for GDS Service Portal so that portal users can take advantage of intelligent query features and find the answers they need.

### Before you begin

Role required: admin or sp\_admin

**Note:**

AI Search is enabled in Service Portal for all new and zBoot customers by default.

If you're upgrading to Australia as an existing customer, AI Search is inactive in Service Portal by default. You can enable it by updating the portal record.

If you leave AI Search inactive, the portal uses the legacy search experience.

### About this task

Using AI Search, GDS Service Portal users can find answers with features like auto-complete search queries, natural language support, and typo handling.

### Procedure

1.  Navigate to **Service Portal** &gt; **Portals** and open a portal record.

2.  On the form, select **Enable AI Search**.

3.  In the **Search Application** field, select the search application configuration to use for the portal.

    A search application configuration defines search experience settings, such as the search engine, search results limit, and suggestions limit. A search application configuration is selected by default, but you can select a different configuration if needed.

    For more information on defining a search application configuration, see [Defining search application configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/defining-search-app-cfgs-ais.md).

4.  In the **Search Results Configuration** field, select the search results configuration to enable for the portal.

    A search results configuration defines how search results are displayed. A search results configuration is selected by default, but you can select a different configuration if needed.

    For more information on defining a search results configuration, see [Create an EVAM definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/define-composite-dataset.md).

5.  Select **Update**.


### Result

AI Search is enabled throughout the portal, and constituents can use AI Search the next time they log in.

The Search Sources related list is hidden from the portal record. You now define search sources in the AI Search application. For more information, see [Defining search sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-sources-ais.md) and [Link a search source to a search profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/link-search-source-profile-ais.md).

To use AI Search for knowledge articles, you can keep the default **Knowledge Bases** search source or select a custom one.

### What to do next

Search widgets that you cloned or customized before a system upgrade may not be compatible with AI Search. You can resolve this issue by running a fix script that reclassifies search widget instances. For more information, see [Reclassify cloned or customized search widgets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/reclassify-search-widgets.md).

