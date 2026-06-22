---
title: Configure the GOV.UK Design System Service Portal User Profile page
description: Configure the user profile page using widgets and widget instances, enabling UK citizens to view and manage their personal profiles, preferences, and activity history.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/public-sector-digital-services/psds-config-gds-profile-page.html
release: australia
product: Public Sector Digital Services
classification: public-sector-digital-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure pages, Configure UK GDS Service Portal, GOV.UK Developer Toolkit, Set up self-service, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure the GOV.UK Design System Service Portal User Profile page

Configure the user profile page using widgets and widget instances, enabling UK citizens to view and manage their personal profiles, preferences, and activity history.

This page provides the basic structure for a GDS-conforming user profile page that specifies details about an user like their name, company, title, and location. By default, the User Profile page contains the following widgets that can be customized or removed:

-   Header widget, which controls which options appear in the page header. Contains GOV.UK logo, global navigation, language selector, notifications, user profile.

    **Note:** This widget cannot be cloned for modification. Instead, configure the header menu by associating the header menu with a portal. For more information on configuring a header menu, see [Configure a portal header menu](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/configure-header-menu.md).

-   Breadcrumbs widget, which displays information based on where a page is located in a portal, allowing users to navigate around.

    **Note:** You can customize this widget only to change the breadcrumb path. For more information, see [KB0719179](https://support.servicenow.com/kb_view.do?sysparm_article=KB0719179).

-   User Profile portal widget, which displays profile photo, name, contact details, and other user profile information.

    **Note:** You can use this base system widget as-is on the User Profile portal page, modify the widget instance \(which makes changes on this page **only**\), or clone it to make modifications across multiple pages that suit your own business needs. For more information on how to clone widgets and use widget instances, see [Configure the GOV.UK Design System Service Portal Widgets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-widgets.md).

-   Footer Widget, which displays support links, other resources, and legal disclaimers.

    **Note:** Add or edit a footer for your portal by configuring it in the Theme form. For more information on adding a footer to a portal, see [Add a header or footer to a portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/configure-header-menu.md).


.

For more information on how to edit widgets that appear on a page in the Service Portal Designer, see [Configure the GOV.UK Design System Service Portal Pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-pages.md). For more information on portal pages, see [Create and edit a page using the Service Portal Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/t_ConfigureAPage.md).

**Parent Topic:**[Configure the GOV.UK Design System Service Portal Pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-pages.md)

