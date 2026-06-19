---
title: Configure the GOV.UK Design System \(GDS\) Service Portal
description: Customize and modify the GOV.UK Design System Service Portal to meet your needs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/public-sector-digital-services/psds-config-gds-content-pack-gsp.html
release: australia
product: Public Sector Digital Services
classification: public-sector-digital-services
topic_type: concept
last_updated: "2026-06-01"
reading_time_minutes: 7
breadcrumb: [GOV.UK Developer Toolkit, Set up self-service, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure the GOV.UK Design System \(GDS\) Service Portal

Customize and modify the GOV.UK Design System Service Portal to meet your needs.

The GOV.UK Design System Service Portal \(/ukgds\) is a Service Portal with a library of configurable widgets and pages \(catalog, case list, case details, knowledge articles, and record producer​\) that resemble the GOV.UK design system, and follow the patterns that GOV.UK dictates. The GOV.UK Design System Service Portal comes default with the GOV.UK Developer Toolkit.​

A portal is the engine that contains all references to the content that constituents will see in their end-user experience. The portal record defines the URL extension for a site, the portal's knowledge base, its catalog, and its homepage. The portal record can also be used to define the header menu and portal branding. With the GOV.UK Developer Toolkit, you can use the base system GOV.UK Design System Service Portal that is provided for you, or you may add any number of GDS-adherant portal widgets and pages provided with the Developer Toolkit to an existing portal. For a list of widgets included in the GOV.UK Developer Toolkit widget library, see [GDS Service Portal Widget Library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-widget-lib.md)

After installation of the GOV.UK Developer Toolkit, you can customize the default GOV.UK Design System Service Portal to add or change widgets, themes, and branding, and can configure page and widget access by role.

Some of the components that you can customize include:

-   **Branding**: [Configure the portal branding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-gds-theme.md) to give your GOV.UK Design System Service Portal its own look and feel. For example, you can give your portal a name, add your logo, and customize the colors.
-   **Menus**: [Configure the portal header menu](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-gds-theme.md) to set up the main menu, one of the main navigation controls for your users.
-   **Homepage**[Configure the portal homepage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-gds-homepage.md).
-   **Widgets**: [Use Service Portal widgets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-widgets.md) to define the content and behavior of your portal.
-   **Roles**: Configure page/widget security by role to either set up pages or widgets to be public \(no authentication required\), or to filter them by user role. By default, all pages in the GDS Service Portal, except the login and registration pages, require authentication to be accessed.

## Configuration Overview

This workflow provides a high-level overview for configuring the GDS Service Portal, after you have [installed the GOV.UK Developer Toolkit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-install-gds-content-pack.md).

1.  [Configure the base-system GDS Service Portal record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-gds-portal-record.md)

    A base system GOV.UK Design System Service Portal is provided with the [installed the GOV.UK Developer Toolkit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-install-gds-content-pack.md) that can be modified using widgets and pages to fit your needs. The portal record defines the URL extension for an agency's portal site \(which for the GDS Service Portal is, by default, /ukgds\), and things like the knowledge base, catalog, record producers, and homepage. You can also use the portal record to define the header menu and the portal branding.

2.  [Configure the portal branding and theme](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-gds-theme.md)

    With the Branding Editor, you can configure the styles and theme of the GOV.UK Design System Service Portal with real-time updates, allowing you to see how your portal appears to users. By default, the GDS Service Portal theme adheres to standards set forth by the UK government for branding, accessibility, and responsive design. The default portal theme supplies standardized color palettes, typography, and styling for GDS Service Portal components, and styled headers, footers, search widgets, breadcrumbs, and knowledge pages, aligned with Gov.UK standards.

3.  Configure [portal pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-pages.md) and [widgets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-widgets.md).

    Pages are the centerpiece of the end-user portal experience. By default, the GOV.UK Developer Toolkit provides a library of already-configured portal pages that contain the neccessary components that are set forth by GOV.UK Design System guidelines, and can be customized to fit your needs. You can also use any existing base system pages as examples when creating new pages from scratch.

    Widgets are what define the content of your pages. By default, the GOV.UK Developer Toolkit provides a library of already-configured widgets that adhere to GOV.UK Design System guidelines, display relevant information, and can be customized to display different variations of information. You can use the base system widgets provided with the GOV.UK Developer Toolkit to get started configuring portal pages.

4.  [Configure search in the portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-search.md)

    Search data displays within a widget on the search page. To make data searchable from a portal, create a search source that fetches data from a single table within your instance, from multiple tables, or from an external site. Enable AI Search to allow constituents to take advantage of intelligent query features and find the answers they need.

5.  [Manage access to the portal]()

    Manage who can access the GDS Service Portal by making pages or widgets public, configuring login and single sign-on \(SSO\), or limiting page access by role. You can also use advanced user criteria for access to pages, widgets, and more.


-   **[Configure the GOV.UK Design System Service Portal theme](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-gds-theme.md)**  
Use the Branding Editor to give the GDS Service Portal its own look and feel.
-   **[Configure the GOV.UK Design System Service Portal record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-gds-portal-record.md)**  
Use the portal record on the platform UI to change components of your GDS Service Portal.
-   **[Configure the GOV.UK Design System Service Portal Pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-pages.md)**  
By default, the GOV.UK Developer Toolkit supplies you with pages that can be used as-is, or customized by adding and removing widgets in Service Portal Designer.
-   **[Configure the GOV.UK Design System Service Portal Widgets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-widgets.md)**  
Configurable portal widgets provide you with the ability to configure the behavior, content, and layout of the GOV.UK Design System Service Portal by configuring widget settings and instance options. Use the base system widgets included with the GDS Service Portal to get started configuring portal pages.
-   **[Configure GOV.UK Design System Service Portal Catalog Items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-catalog.md)**  
Use the Service Catalog and the Service Catalog widgets to add or edit existing items to the GDS Service Portal catalog.
-   **[Configure GOV.UK Design System Service Portal Knowledge Base](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-kb.md)**  
Use Knowledge Base widgets to build a knowledge base for your GDS Service Portal.
-   **[Configure GDS Service Portal Search Widgets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-search.md)**  
Configure and use search widgets for GDS Service Portal so that portal users can take advantage of intelligent query features and find the answers they need.
-   **[]()**  


**Parent Topic:**[Configure GOV.UK Developer Toolkit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-dev-toolkit.md)

**Previous topic:**[Install the GOV.UK Developer Toolkit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-install-gds-content-pack.md)

**Next topic:**[Configure the GOV.UK Design System Service Portal theme](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-gds-theme.md)

