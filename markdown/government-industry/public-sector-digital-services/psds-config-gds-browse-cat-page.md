---
title: Configure the GOV.UK Design System Service Portal Services Page
description: Configure the Services page, which enables constituents to browse and search catalog items from different service catalogs and categories and see all services available to them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/public-sector-digital-services/psds-config-gds-browse-cat-page.html
release: australia
product: Public Sector Digital Services
classification: public-sector-digital-services
topic_type: concept
last_updated: "2026-06-01"
reading_time_minutes: 2
breadcrumb: [Configure pages, Configure UK GDS Service Portal, GOV.UK Developer Toolkit, Set up self-service, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure the GOV.UK Design System Service Portal Services Page

Configure the Services page, which enables constituents to browse and search catalog items from different service catalogs and categories and see all services available to them.

This page provides the basic structure for a GDS-conforming service catalog homepage that lists the services available to constituents from that catalog. Catalog items may be grouped into categories, which can also contain one or more subcategories. By default, the first 10 items in a category appear under the category name on the service catalog home page.

\[Omitted image "psds\_uk\_gds\_services.png"\] Alt text: GDS Portal service catalog Landing page.

By default, the Services page contains the following widgets that can be customized or removed:

-   Header widget, which controls which options appear in the page header. Contains GOV.UK logo, global navigation, language selector, notifications, user profile.

    **Note:** This widget cannot be cloned for modification. Instead, configure the header menu by associating the header menu with a portal. For more information on configuring a header menu, see [Configure a portal header menu](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/configure-header-menu.md).

-   Breadcrumbs widget, which displays information based on where a page is located in a portal, allowing users to navigate around.

    **Note:** You can customize this widget only to change the breadcrumb path. For more information, see [KB0719179](https://support.servicenow.com/kb_view.do?sysparm_article=KB0719179).

-   Catalog Search widget and Typeahead Search widget, which displays a search box that navigates to the search results page with information specific to the service catalog.
-   UK GDS SC Categories widget, which displays the service catalog categories through the catalog selector dropdown and category tree in the sidebar.

    **Note:** This widget renders the categories available in this widget from the Categories table in Service Catalog \[sc\_category\]. For more information on associating your portal with catalogs, see [Configure a catalog in Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/associate-portal-catalog.md) and [Configure GOV.UK Design System Service Portal Catalog Items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-catalog.md).

-   UK GDS SC Category Page widget, which lists the service catalog items available within a certain category.

    **Note:** Categories are determined within the Service Catalog module.

-   Footer Widget, which displays support links, other resources, and legal disclaimers.

    **Note:** Add or edit a footer for your portal by configuring it in the Theme form. For more information on adding a footer to a portal, see [Add a header or footer to a portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/configure-header-menu.md).


.

For more information on how to edit widgets that appear on a page in the Service Portal Designer, see [Configure the GOV.UK Design System Service Portal Pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-pages.md). For more information on portal pages, see [Create and edit a page using the Service Portal Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/t_ConfigureAPage.md).

**Parent Topic:**[Configure the GOV.UK Design System Service Portal Pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-pages.md)

