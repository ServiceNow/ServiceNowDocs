---
title: Homepage Search widget
description: Add a search bar to your home page. You can use this base system widget as-is in your portal or clone it to suit your own business needs.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Search widgets, Widget library, Using portal widgets, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Homepage Search widget

Add a search bar to your home page. You can use this base system widget as-is in your portal or clone it to suit your own business needs.

![Homepage Search widget](../image/HomePageSearch.png "Homepage Search widget")

## Instance options

Use the instance options to configure the Homepage Search widget for a portal page.

**Note:** The AI Search instance options apply only if AI Search is enabled in your portal. For more information on enabling AI Search for Service Portal, see [Enable and configure AI Search in Service Portal](../task/enable-ais-sp.md).

<table id="table_bkp_rsp_5mb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Presentation

</td></tr><tr><td>

Title

</td><td>

Name that appears above the search bar. For example "How can we help?"

</td></tr><tr><td>

Short description

</td><td>

A subtitle that appears below the title.

</td></tr><tr><td>

Typeahead search

</td><td>

Controls the appearance of the search bar. Use a comma separated list inside curly braces to add style details to the search bar, for example \{title: 'Search', color: 'blue', size: 'lg'\}. For more information on which style options you can add, see the instance options for the [Typeahead Search widget](typeahead-search-widget.md).

</td></tr><tr><td class="sub-head" colspan="2">

AI Search

</td></tr><tr><td>

Search Application

</td><td>

Defines search experience settings for the widget, such as the search engine, search results limit, and suggestions limit. By default, the widget uses the same search application configuration as the portal, but you can override this configuration at the widget level.

 For more information on defining a search application configuration, see [Defining search application configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/defining-search-app-cfgs-ais.md).

</td></tr><tr><td>

Search Results Configuration

</td><td>

Defines how search results are displayed after using the widget. By default, the widget uses the same search results configuration as the portal, but you can override this configuration at the widget level.

 For more information on defining a search results configuration, see [Define a composite dataset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/entity-view-action-mapper-evam/define-composite-dataset.md).

</td></tr><tr><td>

Disable All Suggestions

</td><td>

Option to disable search suggestions.

</td></tr><tr><td>

Placeholder

</td><td>

Text that appears in the search box before the user enters anything. By default, the placeholder text is `How can we help?`.

</td></tr><tr><td>

AI Search Source Filter

</td><td>

Content that portal users can search on, including tables in your instance or external data sources. For more information, see [Defining search sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/search-sources-ais.md).

</td></tr></tbody>
</table>**Parent Topic:**[Search widgets](search-widgets.md)

**Related topics**  


[Create and edit a page using the Service Portal Designer](../task/t_ConfigureAPage.md#)

[Configure widget instances](c_ConfigureWidgetInstances.md)

[Clone a widget](../task/t_CloneAndEditAWidget.md)

