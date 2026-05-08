---
title: Catalog Homepage Search widget
description: Give your users the option to search the Service Catalog as soon as they log in. You can use this base system widget as-is in your portal or clone it to suit your own business needs.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Service Catalog widgets, Widget library, Using portal widgets, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Catalog Homepage Search widget

Give your users the option to search the Service Catalog as soon as they log in. You can use this base system widget as-is in your portal or clone it to suit your own business needs.

## Using the widget

Add the Catalog Homepage Search widget on your Service Catalog landing page. When users navigate to the Service Catalog, they can use the Catalog Homepage Search widget to find what they are looking for.

![The Catalog Homepage Search widget](../image/cat-homepage-search.png)

Users can enter a keyword in the search bar. The Catalog Homepage Search widget uses a predictive search feature that shows words as users type.

Alternatively, to navigate to a list of Service Catalog categories, users can select **Browse by Categories**.

## Instance options

Use the instance options to configure the Catalog Homepage Search widget for a portal page.

**Note:** The AI Search instance options apply only if AI Search is enabled in your portal. For more information on enabling AI Search for Service Portal, see [Enable and configure AI Search in Service Portal](../task/enable-ais-sp.md).

<table id="table_ydc_fpv_bkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Presentation

</td></tr><tr><td>

Title

</td><td>

Title to appear above the search bar.

</td></tr><tr><td>

Short description

</td><td>

Text to appear under the title.

</td></tr><tr><td class="sub-head" colspan="2">

AI Search

</td></tr><tr><td>

Search Application

</td><td>

Defines search experience settings for the widget, such as the search engine, search results limit, and suggestions limit. By default, the widget uses the same search application configuration as the portal, but you can override this configuration at the widget level.

 For more information on defining a search application configuration, see Defining search application configurations.

</td></tr><tr><td>

Search Results Configuration

</td><td>

Defines how search results are displayed after using the widget. By default, the widget uses the same search results configuration as the portal, but you can override this configuration at the widget level.

 For more information on defining a search results configuration, see Define a composite dataset.

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

Content that portal users can search on, including tables in your instance or external data sources. For more information, see Defining search sources.

</td></tr><tr><td class="sub-head" colspan="2">

Other Options

</td></tr><tr><td>

Typeahead Search

</td><td>

Configuration of the search bar. You configure the search bar by using the instance options for the [Typeahead Search widget](typeahead-search-widget.md). Use the syntax `{field1:'value1',field2:'value2'}`. For example, to configure the title, color, and size of the search bar, enter the following: `{title:'Search...',color:'default',size:'lg'}`.

</td></tr></tbody>
</table>**Parent Topic:**[Service Catalog widgets](sc-widgets.md)

**Related topics**  


[Catalog Content widget](catalog-content-widget.md)

[Recent &amp; Popular Items widget](recent-and-popular-items-widget.md)

[Request Fields widget](request-fields-widget.md)

[Requested Items widget](requested-items-widget.md)

[Requests and Approvals widget](requests-and-approvals-widget.md)

[SC Catalog Item widget](sc-catalog-item-widget.md)

[SC Categories widget](sc-categories-widget.md)

[SC Category Page widget](sc-category-page-widget.md)

[SC Order Guide widget](sc-order-guide-widget.md)

[SC Popular Items widget](sc-popular-items.md)

[SC Save Bundles widget](save-bundles-widget.md)

[SC Saved Carts widget](saved-cart-widget.md)

[SC Scroll to top widget](sc-scroll-to-top.md)

[SC Shopping Cart widget](sc-shopping-cart.md)

[SP Variable Editor widget](variable-editor-widget.md)

[SC Wish List Cart widget](sc-wish-list.md)

[Create and edit a page using the Service Portal Designer](../task/t_ConfigureAPage.md#)

[Configure widget instances](c_ConfigureWidgetInstances.md)

[Clone a widget](../task/t_CloneAndEditAWidget.md)

