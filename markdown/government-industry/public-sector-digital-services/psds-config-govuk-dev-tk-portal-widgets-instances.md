---
title: Configure Widgets Instances for GDS Service Portal pages
description: You can use widget instances to configure the location, properties, and CSS specific to that instance of the widget. Create unique instances of widgets by configuring the options for each instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-widgets-instances.html
release: australia
product: Public Sector Digital Services
classification: public-sector-digital-services
topic_type: task
last_updated: "2026-06-01"
reading_time_minutes: 3
breadcrumb: [Configure widgets, Configure UK GDS Service Portal, GOV.UK Developer Toolkit, Set up self-service, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure Widgets Instances for GDS Service Portal pages

You can use widget instances to configure the location, properties, and CSS specific to that instance of the widget. Create unique instances of widgets by configuring the options for each instance.

## Before you begin

A page must already be created with widgets added to it. For information on how to create or edit a portal page and add widgets, see [Configure the GOV.UK Design System Service Portal Pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-pages.md). You can also configure the existing widget instances on a base system page. For more information on the base system pages that come with the GOV.UK Developer Toolkit, see [Configure the GOV.UK Design System Service Portal Pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-pages.md).

Role required: admin, sp\_admin

## About this task

Each widget added to a page becomes its own instance. Because widgets are reusable and can appear on different pages to enable the user to do different things, the application of a widget on a page is referred to as a Widget Instance. The page loads with content represented by instances of a widget specific to that page.

Widget instances get their logic from the base widget template, client scripts, server scripts, and depending on the widget, CSS.

You can have several instances of the same widget on a page, and each instance of the widget you configure remains unique. For example, each instance of a Knowledge widget on a page could map to a different knowledge base, or be organized in a different way.

Adding a widget to a page creates a new Widget Instance, as well as a record on the Widget Instances \[sp\_instance\] table with the following information:

-   A reference to the widget
-   A reference to the column of the page where the widget is located
-   The configuration for a widget in the form of pre-defined form fields and an **Additional Options** field in JSON format

You can use widget instances to configure the location, properties, and CSS specific to that instance of the widget.

**Note:** For widgets that do not contain any information by default, you must configure the options for their widget instances before they will appear on a portal page.

For more information on configuring widget instances, see [Configure Widgets Instances for GDS Service Portal pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-widgets-instances.md).

For information on how to clone and edit a default GDS Service Portal widget, see [Customize Widgets for GOV.UK Design System Service Portal pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-widgets-edit.md).

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Service Portal Configuration**

2.  Select **Designer**.

3.  Select the page with the widget instance\(s\) you want to configure.

4.  In the Service Portal Designer, move to a widget instance and select the **Edit** icon.

5.  In the instance options window, fill in the fields to configure the widget instance.

6.  Select **Save**.


**Parent Topic:**[Configure the GOV.UK Design System Service Portal Widgets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-widgets.md)

