---
title: Catalog Homepage Search widget
description: Give your users the option to search the Service Catalog as soon as they log in. You can use this base system widget as-is in your portal or clone it to suit your own business needs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-user-interface/service-portal/cat-homepage-search-widget.html
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

\[Omitted image "cat-homepage-search.png"\] Alt text: The Catalog Homepage Search widget

Users can enter a keyword in the search bar. The Catalog Homepage Search widget uses a predictive search feature that shows words as users type.

Alternatively, to navigate to a list of Service Catalog categories, users can select **Browse by Categories**.

## Instance options

Use the instance options to configure the Catalog Homepage Search widget for a portal page.

**Note:** The AI Search instance options apply only if AI Search is enabled in your portal. For more information on enabling AI Search for Service Portal, see [Enable and configure AI Search in Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/enable-ais-sp.md).

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

 For more information on defining a search application configuration, see [Defining search application configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/defining-search-app-cfgs-ais.md).

</td></tr><tr><td>

Search Results Configuration

</td><td>

Defines how search results are displayed after using the widget. By default, the widget uses the same search results configuration as the portal, but you can override this configuration at the widget level.

 For more information on defining a search results configuration, see [Define a composite dataset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/define-composite-dataset.md).

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

Content that portal users can search on, including tables in your instance or external data sources. For more information, see [Defining search sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-sources-ais.md).

</td></tr><tr><td class="sub-head" colspan="2">

Other Options

</td></tr><tr><td>

Typeahead Search

</td><td>

Configuration of the search bar. You configure the search bar by using the instance options for the [Typeahead Search widget](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/typeahead-search-widget.md). Use the syntax `{field1:'value1',field2:'value2'}`. For example, to configure the title, color, and size of the search bar, enter the following: `{title:'Search...',color:'default',size:'lg'}`.

</td></tr></tbody>
</table>**Parent Topic:**[Service Catalog widgets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/sc-widgets.md)

**Related topics**  


[Catalog Content widget]()

[Recent &amp; Popular Items widget]()

[Request Fields widget]()

[Requested Items widget]()

[Requests and Approvals widget]()

[SC Catalog Item widget]()

[SC Categories widget]()

[SC Category Page widget]()

[SC Order Guide widget]()

[SC Popular Items widget]()

[SC Save Bundles widget]()

[SC Saved Carts widget]()

[SC Scroll to top widget]()

[SC Shopping Cart widget]()

[SP Variable Editor widget]()

[SC Wish List Cart widget]()

[Create and edit a page using the Service Portal Designer]()

[Configure widget instances]()

[Clone a widget]()

