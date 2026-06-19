---
title: Configure the GOV.UK Design System Service Portal Widgets
description: Configurable portal widgets provide you with the ability to configure the behavior, content, and layout of the GOV.UK Design System Service Portal by configuring widget settings and instance options. Use the base system widgets included with the GDS Service Portal to get started configuring portal pages.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-widgets.html
release: australia
product: Public Sector Digital Services
classification: public-sector-digital-services
topic_type: concept
last_updated: "2026-06-01"
reading_time_minutes: 6
breadcrumb: [Configure UK GDS Service Portal, GOV.UK Developer Toolkit, Set up self-service, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure the GOV.UK Design System Service Portal Widgets

Configurable portal widgets provide you with the ability to configure the behavior, content, and layout of the GOV.UK Design System Service Portal by configuring widget settings and instance options. Use the base system widgets included with the GDS Service Portal to get started configuring portal pages.

The GDS Service Portal uses widgets for configuration. Widgets are what define the content of your portal pages. You can use the base system widgets provided with the GOV.UK Developer Toolkit in their default state, or you can clone, modify, or develop custom widgets to better fit your needs.

**Note:** Base system widgets are read-only so you can benefit from future updates. To make changes, you can clone base system widgets. However, cloned widgets are considered custom and don't benefit from future updates to the widgets they were cloned from. To learn more about cloning or creating widgets, see .

When you create or update a page in the Service Portal Designer, you can add widgets to that page by searching in the widget filter and dragging a widget onto the page. You can then configure widget behavior, visual appearance, and content to update the information presented on the widgets. Each time you add a widget to a page, an instance of that widget is created that can be modified individually for use on that page. For each instance of a base system widget that you add to a page, you can configure the instance options available for that widget.

For a list of base system widgets that enable you to configure various pages within the GOV.UK Design System Service Portal, see [Widget Library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-widget-lib.md). You can also access all widget records from the platform at **All** &gt; **Service Portal** &gt; **Widgets**.

There are four main categories of widgets available for use with the GDS Service Portal.

## Service Catalog widgets

Service Catalog widgets let you browse, request, and track services directly from the GDS Service Portal. They provide the building blocks for a complete Service Catalog experience, allowing users to find what they need and submit requests in one central place.

Service Catalog widgets allow portal users to do the following:

-   Browse available services and catalog items.
-   Search the catalog from the portal homepage.
-   View services by category and submit requests.
-   Track requests and approvals.

These widgets display service information in a streamlined, task‑focused way. For example, some widgets help users search or browse the catalog, while others let users view request details or check the status of services they have already requested. As an admin, you can use the Service Catalog widgets to build a catalog for your portal.

## Knowledge Management widgets

Knowledge Management widgets enable users to search, browse, and read knowledge articles directly in the GDS Service Portal, so they can find answers to their questions and learn how to use services without contacting support. These widgets provide the core components for building a knowledge experience that can help them find answers quickly and consistently. For more information on creating and maintaining the articles that are shown on the Knowledge Management widgets, see .

Constituents can use Knowledge Management widgets to do the following:

-   Search the knowledge base for information and solutions.
-   Browse knowledge bases and categories.
-   View knowledge articles and related content.
-   See popular, featured, or top‑rated articles.
-   Interact with articles by rating or commenting, when available.

These widgets organize knowledge content in a clear, navigational way. Some widgets help users discover articles through search and filters, while others display article details and related information on the article page. As an admin, you can use Knowledge Management widgets to build a knowledge base for your portal. For more information on maintaining a knowledge base within a portal, see [Configure Knowledge Base](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-kb.md).

## Service Portal configuration page widgets

Service Portal configuration page widgets help you set up and manage your Service Portal experience. Use these widgets when you configure portals, pages, themes, and widgets in the Service Portal Configuration workspace. These widgets support portal configuration tasks such as:

-   Navigating Service Portal configuration pages.
-   Viewing portals and pages in a structured, tree‑based layout.
-   Editing portal themes and previewing design changes.
-   Configuring pages and widgets using visual editors.

Service Portal configuration page widgets run behind the scenes and are internal to the configuration experience. For example, they power tools like the Portal Map, Page Map, Branding Editor, and Widget Editor, helping you understand and manage how your portal is structured and displayed.

As an admin, navigate to **Service Portal** &gt; **Service Portal Configuration**to use these widgets.

## Search widgets

Service Portal search widgets let you find information quickly across the GDS Service Portal. Use these widgets to search for knowledge articles, catalog items, records, and other content without navigating through multiple pages.

Search widgets help users to do the following:

-   Search for answers, services, and records from a single search bar.
-   See relevant results as they type with predictive search.
-   Filter and refine search results to find what they need.
-   Get suggested or context‑aware results while submitting requests.

Service Portal search widgets work in different locations, such as the portal homepage, search results page, or within record producers. Some widgets display a search bar, while others show detailed results with filters and facets for easier discovery. As an admin, you can configure search in Service Portal using any of the search widgets by navigating to **Service Portal** &gt; **Service Portal Configuration** and adding widgets to a page. For a list of Search Widgets available by default in the GDS Service Portal, see [Widget Library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-widget-lib.md).

## Example widgets

Service Portal example widgets help show what you can do in theGDS Service Portal. These widgets demonstrate how common portal features work and what information you can access directly from a portal page, serving as example code for how scripts are used in a widget.

Example widgets help users to do the following:

-   Search for answers, services, and records from a single search bar.
-   See relevant results as they type with predictive search.
-   Filter and refine search results to find what they need.
-   Get suggested or context‑aware results while submitting requests.

These widgets appear as ready‑to‑use components in the GDS Service Portal configuration. Some focus on everyday tasks, such as approving requests or changing a password, while others show interactive or informational elements you might see on a portal page.

As an admin, you can use the example widgets to see how to use HTML, CSS, or client and server scripts in the GDS Service Portal, and clone and extend each widget to suit your needs. For a list of example Widgets available by default in the GDS Service Portal, see [Widget Library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-widget-lib.md).

For more information on using configurable widgets in portals, see .

-   **[Customize Widgets for GOV.UK Design System Service Portal pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-widgets-edit.md)**  
You can use base system widgets as-is in the GDS Service Portal, or you may clone them to suit your needs.
-   **[Add Widgets to GOV.UK Design System Service Portal pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-widgets-add.md)**  
Add widgets to your portal pages and modify its data, presentation, and behavior. You can use base system widgets as-is in the GDS Service Portal, or you may clone them to suit your needs.
-   **[Configure Widgets Instances for GDS Service Portal pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-widgets-instances.md)**  
You can use widget instances to configure the location, properties, and CSS specific to that instance of the widget. Create unique instances of widgets by configuring the options for each instance.

**Parent Topic:**[Configure the GOV.UK Design System \(GDS\) Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-gds-content-pack-gsp.md)

