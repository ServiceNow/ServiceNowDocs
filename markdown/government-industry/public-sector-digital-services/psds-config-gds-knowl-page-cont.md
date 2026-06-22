---
title: Configure the GOV.UK Design System Service Portal Knowledge Pages
description: The knowledge pages provide the basic, GDS-compliant structure for displaying knowledge base content for constituents using the GDS Service Portal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/public-sector-digital-services/psds-config-gds-knowl-page-cont.html
release: australia
product: Public Sector Digital Services
classification: public-sector-digital-services
topic_type: concept
last_updated: "2026-06-04"
reading_time_minutes: 4
breadcrumb: [Configure pages, Configure UK GDS Service Portal, GOV.UK Developer Toolkit, Set up self-service, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure the GOV.UK Design System Service Portal Knowledge Pages

The knowledge pages provide the basic, GDS-compliant structure for displaying knowledge base content for constituents using the GDS Service Portal.

By default, the GOV.UK Developer Toolkit comes with base system knowledge pages, which contain the following widgets.

Most widgets can be configured by cloning and modifying, or you can use the instance options where available to configure widgets for a portal page. For more information on the instance options available for each widget, see [Portal Widget Library.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-widget-lib.md)

## Knowledge Home

\[Omitted image "psds\_gds\_knowledge\_homepage.png"\] Alt text:

The Knowledge homepage contains the following widgets:

-   Knowledge Banner Header widget, which controls which options appear in the page header. Contains GOV.UK logo, global navigation, language selector, notifications, user profile.

    **Note:** This widget cannot be cloned for modification. Instead, configure the header menu by associating the header menu with a portal. For more information on configuring a header menu, see [Configure a portal header menu](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/configure-header-menu.md).

-   Knowledge Featured Articles widget, which displays profile photo, name, contact details, and other user profile information.
-   Knowledge Most Viewed Articles widget, which displays the most viewed knowledge base articles.
-   Knowledge Most Useful Articles widget, which displays profile photo, name, contact details, and other user profile information.
-   Knowledge Base Categories widget, which displays profile photo, name, contact details, and other user profile information.
-   Footer Widget, which displays support links, other resources, and legal disclaimers.

    **Note:** Add or edit a footer for your portal by configuring it in the Theme form. For more information on adding a footer to a portal, see [Add a header or footer to a portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/configure-header-menu.md).


## Knowledge Search

\[Omitted image "psds\_gds\_knowledge\_search\_page.png"\] Alt text:

The Knowledge search page contains the following widgets:

-   Knowledge Banner Header widget, which controls which options appear in the page header. Contains GOV.UK logo, global navigation, language selector, notifications, user profile.

    **Note:** This widget cannot be cloned for modification. Instead, configure the header menu by associating the header menu with a portal. For more information on configuring a header menu, see [Configure a portal header menu](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/configure-header-menu.md).

-   Knowledge Base Breadcrumbs widget, which displays information based on where an article is located in a knowledge base. You can broaden your search of the knowledge base to include all of the articles in a particular category by selecting the titles in the breadcrumbs. This widget also includes a search box so that you can search for an article by name.

    **Note:** You can customize this widget only to change the breadcrumb path. For more information, see [KB0719179](https://support.servicenow.com/kb_view.do?sysparm_article=KB0719179).

-   Knowledge Search widget which displays search information specifically confined to the knowledge base.
-   Knowledge Selected Filter widget, which displays profile photo, name, contact details, and other user profile information.
-   Knowledge Result widget, which displays profile photo, name, contact details, and other user profile information.
-   Footer Widget, which displays support links, other resources, and legal disclaimers.

    **Note:** Add or edit a footer for your portal by configuring it in the Theme form. For more information on adding a footer to a portal, see [Add a header or footer to a portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/configure-header-menu.md).


## Knowledge Article View

The Knowledge Article view page displays knowledge base details, including the article number, short description, and article content. You can also give feedback or comment on an article.

\[Omitted image "psds\_gds\_knowledge\_article\_view.png"\] Alt text:

The Knowledge homepage contains the following widgets:

-   Knowledge Banner Header widget, which controls which options appear in the page header. Contains GOV.UK logo, global navigation, language selector, notifications, user profile.

    **Note:** This widget cannot be cloned for modification. Instead, configure the header menu by associating the header menu with a portal. For more information on configuring a header menu, see [Configure a portal header menu](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/configure-header-menu.md).

-   Knowledge Base Breadcrumbs widget, which displays information based on where an article is located in a knowledge base. You can broaden your search of the knowledge base to include all of the articles in a particular category by selecting the titles in the breadcrumbs. This widget also includes a search box so that you can search for an article by name.

    **Note:** You can customize this widget only to change the breadcrumb path. For more information, see [KB0719179](https://support.servicenow.com/kb_view.do?sysparm_article=KB0719179).

-   Knowledge Base Search Widget and Typeahead Search widget, which displays search information specifically confined to the knowledge base, with a predictive text feature that shows words as users type.

    **Note:** The Typeahead Search widget is embedded in the Knowledge Base Search Widget, but each widget has its own instance options. For more information on the instance options available for each widget, see [Portal Widget Library.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-widget-lib.md)

-   Knowledge Article Page widget, which displays Knowledge Base articles within the GDS Service Portal.
-   Knowledge Related Articles widget, which displays profile photo, name, contact details, and other user profile information.
-   Footer Widget, which displays support links, other resources, and legal disclaimers.

    **Note:** Add or edit a footer for your portal by configuring it in the Theme form. For more information on adding a footer to a portal, see [Add a header or footer to a portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/configure-header-menu.md).


**Parent Topic:**[Configure the GOV.UK Design System Service Portal Pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-pages.md)

