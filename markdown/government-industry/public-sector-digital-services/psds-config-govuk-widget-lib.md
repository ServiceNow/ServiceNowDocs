---
title: GOV.UK Developer Toolkit GDS Service Portal Widget Library
description: Configurable Portal widgets provide you with the ability to configure the behavior, content, and layout of the GDS Service Portal by configuring widget settings and instance options.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/public-sector-digital-services/psds-config-govuk-widget-lib.html
release: australia
product: Public Sector Digital Services
classification: public-sector-digital-services
topic_type: concept
last_updated: "2026-06-01"
reading_time_minutes: 7
breadcrumb: [GOV.UK Developer Toolkit reference, Reference, Public Sector Digital Services \(PSDS\)]
---

# GOV.UK Developer Toolkit GDS Service Portal Widget Library

Configurable Portal widgets provide you with the ability to configure the behavior, content, and layout of the GDS Service Portal by configuring widget settings and instance options.

Service Portal uses widgets for configuration. When you configure a page or a widget for a portal in the Service Portal Configuration page, you use Service Portal widgets to do so.

**Note:** Base system widgets are read-only so you can benefit from future updates. To make changes, you can clone base system widgets. However, cloned widgets are considered custom and don't benefit from future updates to the widgets they were cloned from. To learn more about cloning or creating widgets, see .

The following is a list of base-system widgets that are included with the toolkit that enable you to configure various pages within the GDS Service Portal, and their instance options.

## Widget Name

Description.

Instance Options per widget.

Page to configure.

<table id="table_tll_jp2_5y"><thead><tr><th>

Widget

</th><th>

Description

</th></tr></thead><tbody><tr><td>

 

</td><td>

Display access key features and pages from any place in portal. It shows logo, search, profile, and others on level 1 of the header, and menu items on level 2 of the header.The appearance of menu items in level 2 of the header is determined by the Portal Mega Menu widget selected.

</td></tr><tr><td>

 

</td><td>

The menu on the header of the portal home page to navigate to different pages. It displays topics in a menu format organized hierarchically.

</td></tr><tr><td>

 

</td><td>

Display taxonomy topics along with the articles and catalog items related to them.

</td></tr><tr><td>

 

</td><td>

Banner to display the announcements, new product or feature highlights, and important information on the top of the page.

</td></tr><tr><td>

 

</td><td>

Displays multiple banners in a carousel to display information on multiple announcements, features, and products.

</td></tr><tr><td>

 

</td><td>

Display different links for quick access including links to a knowledge article, a catalog item, a custom page, or an external URL. You can also select different layouts for quick links cards.

</td></tr><tr><td>

 

</td><td>

Display a list of articles for quick access. Articles can be selected based on featured articles, most viewed articles and more criteria or can be selected manually.

</td></tr><tr><td>

 

</td><td>

Displays catalog items for important request items based on the criteria.

</td></tr><tr><td>

 

</td><td>

Displays case records according to the filter criteria. You can display case details such as state, update, date, and more in a card format.

</td></tr><tr><td>

 

</td><td>

Displays a list of cases, appointments, work orders, or other records from any ServiceNow table in list or card format.

</td></tr><tr><td>

 

</td><td>

Displays a list of frequently asked articles from a selected knowledge table that are categorized based on knowledge article category or related product.

</td></tr><tr><td>

 

</td><td>

Display important information at the bottom of each page. The information includes company information and logo, site links, external links, and social media links.

</td></tr><tr><td>

 

</td><td>

Display key information of a record from the tables available on ServiceNow® table. Your users can also take related actions on the selected record.

</td></tr><tr><td>

 

</td><td>

Displays topics as cards on your portal page enabling your users to access knowledge articles and catalog items related to a topic displayed on your portal in a Portal Browse Taxonomy widget.

</td></tr></tbody>
</table>You can use these widgets as is, or you can duplicate and edit them to suit your needs. For information on how to clone and edit a default GDS Service Portal widget, see [Customize Widgets for GOV.UK Design System Service Portal pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-widgets-edit.md).

For more information on using configurable widgets in portals, see .

There are ? main categories of widgets available for use with the GDS Service Portal.

## Service Catalog widgets

Service Catalog widgets let you browse, request, and track services directly from the Service Portal. They provide the building blocks for a complete Service Catalog experience, allowing you to find what you need and submit requests in one central place.

Use Service Catalog widgets to do the following:

-   Browse available services and catalog items.
-   Search the catalog from the portal homepage.
-   View services by category.
-   Order catalog items and submit requests.
-   Track your requests and approvals.

These widgets display service information in a clear, task‑focused way. For example, some widgets help you search or browse the catalog, while others let you view request details or check the status of items you have already ordered. For more information, see .

## Knowledge Management widgets

Knowledge Management widgets let you search, browse, and read knowledge articles directly in the GDS Service Portal, so you can find answers to their questions and learn how to use services without contacting support. These widgets provide the core components for building a knowledge experience that helps you find answers quickly and consistently. For more information on creating and maintaining the articles that are shown on the Knowledge Management widgets, see

Use Knowledge Management widgets to do the following:

-   Search the knowledge base for information and solutions.
-   Browse knowledge bases and categories.
-   View knowledge articles and related content.
-   See popular, featured, or top‑rated articles.
-   Interact with articles by rating or commenting, when available.

These widgets organize knowledge content in a clear and easy‑to‑navigate way. Some widgets help you discover articles through search and filters, while others display article details and related information on the article page. For more information, see .

## Service Portal configuration page widgets

Service Portal configuration page widgets help you set up and manage your Service Portal experience. Use these widgets when you configure portals, pages, themes, and widgets in the Service Portal Configuration workspace, rather than for end‑user interaction.

Configuration page widgets are included as part of the Service Portal Configuration Pages plugin \[com.glide.service-portal.config\], which is activated automatically when you activate the Service Portal for Enterprise Service Management plugin \[com.glide.service-portal.esm\].

These widgets support portal configuration tasks such as:

-   Navigating Service Portal configuration pages.
-   Viewing portals and pages in a structured, tree‑based layout.
-   Editing portal themes and previewing design changes.
-   Configuring pages and widgets using visual editors.

Service Portal configuration page widgets run behind the scenes and are internal to the configuration experience. For example, they power tools like the Portal Map, Page Map, Branding Editor, and Widget Editor, helping you understand and manage how your portal is structured and displayed. For more information, see .

## Service Portal Header and Footer page widgets

Service Portal configuration page widgets help you set up and manage your Service Portal experience. Use these widgets when you configure portals, pages, themes, and widgets in the Service Portal Configuration workspace, rather than for end‑user interaction.

These widgets support portal configuration tasks such as:

-   Navigating Service Portal configuration pages.
-   Viewing portals and pages in a structured, tree‑based layout.
-   Editing portal themes and previewing design changes.
-   Configuring pages and widgets using visual editors.

Service Portal configuration page widgets run behind the scenes and are internal to the configuration experience. For example, they power tools like the Portal Map, Page Map, Branding Editor, and Widget Editor, helping you understand and manage how your portal is structured and displayed. For more information, see .

## Search widgets

Service Portal search widgets let you find information quickly across the Service Portal. Use these widgets to search for knowledge articles, catalog items, records, and other content without navigating through multiple pages.

Search widgets help you to do the following:

-   Search for answers, services, and records from a single search bar.
-   See relevant results as you type with predictive search.
-   Filter and refine search results to find what you need faster.
-   Get suggested or context‑aware results while submitting requests.

Service Portal search widgets work in different locations, such as the portal homepage, search results page, or within record producers. Some widgets display a simple search bar, while others show detailed results with filters and facets for easier discovery. For more information, see .

## Widgets and Widget Instances

Each widget added to a page becomes its own instance. Because widgets are reusable and can appear on different pages to allow the user to do different things, the application of a widget on a page is referred to as a Widget Instance. The page loads with content represented by instances of a widget specific to that page.

Widget instances get their logic from the base widget template, client scripts, server scripts, and depending on the widget, CSS.

You can have several instances of the same widget on a page, and each instance of the widget you configure remains unique. For example, each instance of a Knowledge widget on a page could map to a different knowledge base, or be organized in a different way.

Adding a widget to a page creates a new Widget Instance, as well as a record on the Widget Instances \[sp\_instance\] table with the following information:

-   A reference to the widget
-   A reference to the column of the page where the widget is located
-   The configuration for a widget in the form of pre-defined form fields and an **Additional Options** field in JSON format

You can use widget instances to configure the location, properties, and CSS specific to that instance of the widget.

For more information on configuring widget instances, see [Configure Widgets Instances for GDS Service Portal pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-widgets-instances.md).

