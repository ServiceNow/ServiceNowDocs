---
title: Faceted Search widget
description: The Faceted Search widget displays search results and search facets defined for a search source. The Faceted Search widget enables end users to filter search results for a more meaningful result set.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Search widgets, Widget library, Using portal widgets, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Faceted Search widget

The Faceted Search widget displays search results and search facets defined for a search source. The Faceted Search widget enables end users to filter search results for a more meaningful result set.

## Using the widget

You can use facet filters to refine your search in Service Portal. For example, you can view only knowledge article search results by selecting the **Knowledge** source facet bucket. Or, to filter search results by certain knowledge categories, you can select one or more facets.

![Filter for faceted Search widget showing "email" search results with available facet filters](../image/faceted-search-widget.png "Filter for Faceted Search widget")

The available facets are dynamic, showing only field values that are included in your current search results. As you select facets, the search narrows and the number of available facets decreases. You can broaden your search by clearing an individual facet selection.

To see which facets you've selected, view the pills in the Filters panel. If you select a different source facet bucket, your other selected facets are carried over and applied to your modified search.

You can initiate a new search by entering a new search term in the typeahead search box. After you enter the new search term, the system clears your facet filter selections from the previous search. You can refine your new search by selecting new facet filters.

For more information on configuring the available facets, see Create a facet in an AI Search application configuration.

## Instance options

Use the instance options to configure the Faceted Search widget for a portal page.

<table id="table_rm5_ksh_zz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Presentation

</td></tr><tr><td>

Facet List Title

</td><td>

Display title for the facet component.

</td></tr><tr><td>

Typeahead Search - Title

</td><td>

Default text in the typeahead search component.

</td></tr><tr><td>

Typeahead Search - Color

</td><td>

Whether the glyph in the typeahead component is filled in.

</td></tr><tr><td>

Typeahead Search - Glyph

</td><td>

Icon that appears in the search field beside the widget. The search icon is the default. To use a different icon, type the name of the icon in the field, for example `search-plus`. For a list of icons to choose from, open the instance options for the Icon Link widget.

</td></tr><tr><td>

Typeahead Search - Size

</td><td>

Determines the font size and height of the widget. Choose from xs, sm, md, and lg.

</td></tr><tr><td>

Show Typeahead Search Box

</td><td>

Option to show or hide the search box on the portal page.

</td></tr><tr><td class="sub-head" colspan="2">

Behavior

</td></tr><tr><td>

Max results for All search

</td><td>

Maximum number of results that display for all search sources when viewed together.

</td></tr><tr><td>

Max results for single search source

</td><td>

Maximum number of results that display for a single search source.

</td></tr><tr><td>

Show Did You Mean

</td><td>

Displays suggestions when a search produces no results.

</td></tr><tr><td>

Typeahead Search - Limit

</td><td>

Number of typeahead search results displayed. The default is 15.

</td></tr><tr><td class="sub-head" colspan="2">

AI Search

</td></tr><tr><td>

Placeholder

</td><td>

Text that appears in the search box before the user enters anything. By default, the placeholder text is `Search`.

 **Note:** This instance option applies only if AI Search is enabled in your portal. For more information on enabling AI Search for Service Portal, see [Enable and configure AI Search in Service Portal](../task/enable-ais-sp.md).

</td></tr></tbody>
</table>**Parent Topic:**[Search widgets](search-widgets.md)

**Related topics**  


[Create and edit a page using the Service Portal Designer](../task/t_ConfigureAPage.md#)

[Configure widget instances](c_ConfigureWidgetInstances.md)

[Clone a widget](../task/t_CloneAndEditAWidget.md)

