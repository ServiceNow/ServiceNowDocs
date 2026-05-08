---
title: Typeahead Search widget
description: Predictive search feature that shows words as users type. You can use this base system widget as-is in your portal or clone it to suit your own business needs.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Search widgets, Widget library, Using portal widgets, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Typeahead Search widget

Predictive search feature that shows words as users type. You can use this base system widget as-is in your portal or clone it to suit your own business needs.

![Typeahead Search widget](../image/WidgetTypeaheadSearch.png "Typeahead Search widget")

## Instance options

Use the instance options to configure the Typeahead Search widget for a portal page.

**Note:** The AI Search instance options apply only if AI Search is enabled in your portal. For more information on enabling AI Search for Service Portal, see [Enable and configure AI Search in Service Portal](../task/enable-ais-sp.md).

<table id="table_ghq_ddf_kz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Presentation

</td></tr><tr><td>

Title

</td><td>

The name or words that appear in the search field before a user starts typing. For example, `search` or `what are you looking for`

</td></tr><tr><td>

Color

</td><td>

Whether the search button beside the search field is filled in or not

</td></tr><tr><td>

glyph

</td><td>

The icon that appears in the search field beside the widget. The search icon is the default. To use a different icon, type the name of the icon in the field, for example `search-plus`. For a list of icons to choose from, open the instance options for the Icon Link widget.

</td></tr><tr><td>

Size

</td><td>

Determines the font size and height of the widget. Choose from xs, sm, md, and lg.

</td></tr><tr><td class="sub-head" colspan="2">

Behavior

</td></tr><tr><td>

Limit

</td><td>

If search suggestions is enabled, enter the number of suggestion entries you want to display. If search suggestions is disabled, enter the number of typeahead entries you want to display. The default is 15. See [Enable and disable search suggestions](https://www.servicenow.com/docs/access?context=enable-search-suggestions&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Contextual Search Sources

</td><td>

Limit the results available in the typeahead search by only configuring specific search sources. For example, users searching in the Service Catalog only see results for the Service Catalog when that search sources is configure. For more information on contextual search, see [Configure Search Sources available on a page](configure-contextual-search.md)

</td></tr><tr><td class="sub-head" colspan="2">

AI Search

</td></tr><tr><td>

Search Application

</td><td>

Defines search experience settings for the widget, such as the search engine, search results limit, and suggestions limit. By default, the widget uses the same search application configuration as the portal, but you can override this configuration at the widget level.

 For more information on defining a search application configuration, see [Defining search application configurations](https://www.servicenow.com/docs/access?context=defining-search-app-cfgs-ais&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Search Results Configuration

</td><td>

Defines how search results are displayed after using the widget. By default, the widget uses the same search results configuration as the portal, but you can override this configuration at the widget level.

 For more information on defining a search results configuration, see [Define a composite dataset](https://www.servicenow.com/docs/access?context=define-composite-dataset&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

Disable All Suggestions

</td><td>

Option to disable search suggestions.

</td></tr><tr><td>

Placeholder

</td><td>

Text that appears in the search box before the user enters anything.

 By default, the placeholder text is `Search`.

</td></tr><tr><td>

AI Search Source Filter

</td><td>

Content that portal users can search on, including tables in your instance or external data sources. For more information, see [Defining search sources](https://www.servicenow.com/docs/access?context=search-sources-ais&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr></tbody>
</table>**Parent Topic:**[Search widgets](search-widgets.md)

**Related topics**  


[Create and edit a page using the Service Portal Designer](../task/t_ConfigureAPage.md#)

[Configure widget instances](c_ConfigureWidgetInstances.md)

[Clone a widget](../task/t_CloneAndEditAWidget.md)

