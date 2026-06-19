---
title: Configure the GOV.UK Design System Service Portal Case List page
description: Configure the case list page.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/public-sector-digital-services/psds-config-gds-case-list-page.html
release: australia
product: Public Sector Digital Services
classification: public-sector-digital-services
topic_type: concept
last_updated: "2026-06-01"
reading_time_minutes: 2
breadcrumb: [Configure pages, Configure UK GDS Service Portal, GOV.UK Developer Toolkit, Set up self-service, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure the GOV.UK Design System Service Portal Case List page

Configure the case list page.

This page provides the basic structure for a GDS-conforming case list page that enables a constituent to access all cases they can view or act on in the GDS Service Portal. This may include cases they have submitted, or cases that have been submitted on their behalf.

\[Omitted image "psds\_uk\_gds\_case\_list.png"\] Alt text: GDS Portal case list page.

By default, the Case List page contains the following widgets that can be customized or removed:

-   Header widget, which controls which options appear in the page header. Contains GOV.UK logo, global navigation, language selector, notifications, user profile.

    **Note:** This widget cannot be cloned for modification. Instead, configure the header menu by associating the header menu with a portal. For more information on configuring a header menu, see .

-   Breadcrumbs widget, which displays information based on where a page is located in a portal, allowing users to navigate around.

    **Note:** You can customize this widget only to change the breadcrumb path. For more information, see [KB0719179](https://support.servicenow.com/kb_view.do?sysparm_article=KB0719179).

-   Search widget and Typeahead Search widget, which displays a search box that navigates to the search results page with a list of cases related to the search query.
-   UK GDS Portal Data List widget, which displays data related to cases from selected case tables in either a list or card format.

    **Note:** JSON parameters control what data categories appear on the Case List page in the GDS Service Portal portal. The Portal Data List widget JSON options define the following 10 case data categories:

    -   All Cases
    -   Action needed
    -   Your cases
    -   Your draft cases
    -   Your requests
    -   Your case tasks
    -   Your service requests
    -   Your information requests
    -   Your licenses/permits
    -   Your social benefits
    You can add new data categories to the GDS Service Portal Case List page by inserting a JSON configuration block into the Portal Data List widget in Service Portal Designer.

-   Footer Widget, which displays support links, other resources, and legal disclaimers.

    **Note:** Add or edit a footer for your portal by configuring it in the Theme form. For more information on adding a footer to a portal, see .


.

For more information on how to edit widgets that appear on a page in the Service Portal Designer, see [Configure the GOV.UK Design System Service Portal Pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-pages.md). For more information on portal pages, see .

**Parent Topic:**[Configure the GOV.UK Design System Service Portal Pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-pages.md)

