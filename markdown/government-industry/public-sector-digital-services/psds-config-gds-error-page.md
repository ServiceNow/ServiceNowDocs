---
title: Configure the Error Pages for GOV.UK Developer Toolkit GDS Service Portal
description: Use Portal Widgets to configure and customize the error page that is shown when a user encounters errors such as broken links, service issues, or downtime \(404, 500, 503\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/public-sector-digital-services/psds-config-gds-error-page.html
release: australia
product: Public Sector Digital Services
classification: public-sector-digital-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure pages, Configure UK GDS Service Portal, GOV.UK Developer Toolkit, Set up self-service, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure the Error Pages for GOV.UK Developer Toolkit GDS Service Portal

Use Portal Widgets to configure and customize the error page that is shown when a user encounters errors such as broken links, service issues, or downtime \(404, 500, 503\).

## About this task

This page provides the basic structure for GDS-compliant, fully responsive error pages \(404, 500, 503\), displaying clear error messages with helpful links. By default, each error page contains the following configurable widgets:

-   Header widget, which controls which options appear in the page header. Contains GOV.UK logo, global navigation, language selector, notifications, user profile.

    **Note:** This widget cannot be cloned for modification. Instead, configure the header menu by associating the header menu with the portal. For more information on configuring a header menu, see [Configure a portal header menu](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/configure-header-menu.md).

-   Error widget, which displays information based on the error encountered.
-   Footer Widget, which displays support links, other resources, and legal disclaimers.

    **Note:** Add or edit a footer to your portal by configuring it in the Theme form. For more information on adding a footer to a portal, see [Add a header or footer to a portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/configure-header-menu.md).


The header, footer, and error message content widgets may be customized to fit your needs using Widget Instances. Optionally, the display of support links or alternative actions can also be configured. For more information on how to configure widgets and widget instances, see [Configure the GOV.UK Design System Service Portal Widgets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-widgets.md).

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **Service Portal** &gt; **Properties**

2.  Select the error page you want to configure, and add a default or customized widget.

    For more information on how to clone edits for modification, see [Configure the GOV.UK Design System Service Portal Widgets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-widgets.md).

3.  In the Default 404 page for Service Portals, type the page ID found in the ID field of the page form and select **Save**.


**Parent Topic:**[Configure the GOV.UK Design System Service Portal Pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-pages.md)

