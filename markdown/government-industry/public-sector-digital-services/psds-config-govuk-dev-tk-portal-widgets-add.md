---
title: Add Widgets to GOV.UK Design System Service Portal pages
description: Add widgets to your portal pages and modify its data, presentation, and behavior. You can use base system widgets as-is in the GDS Service Portal, or you may clone them to suit your needs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-widgets-add.html
release: australia
product: Public Sector Digital Services
classification: public-sector-digital-services
topic_type: task
last_updated: "2026-06-09"
reading_time_minutes: 2
breadcrumb: [Configure widgets, Configure UK GDS Service Portal, GOV.UK Developer Toolkit, Set up self-service, Configure, Public Sector Digital Services \(PSDS\)]
---

# Add Widgets to GOV.UK Design System Service Portal pages

Add widgets to your portal pages and modify its data, presentation, and behavior. You can use base system widgets as-is in the GDS Service Portal, or you may clone them to suit your needs.

## Before you begin

Role required: admin or sp\_admin

**Note:**

If you have not already created the page to which you want to add the widget, see [Configure the GOV.UK Design System Service Portal Pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-pages.md).

## About this task

By default, the GOV.UK Developer Toolkit provides you with a library of reusable portal widgets that follow UK GDS guidelines. Base system widgets are read-only so you can benefit from future updates. To make changes, you can clone base system widgets. For information on how to configure and clone base-system widgets, see [Customize Widgets for GOV.UK Design System Service Portal pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-widgets-edit.md).

## Procedure

1.  Navigate to the **All** &gt; **Service Portal** &gt; **Service Portal Configuration**.

2.  Select **Designer**.

3.  On the Service Portal Designer page, search for and select the page to which you want to add the widget.

4.  Select the **Widgets** tab.

5.  In the Layouts section, drag the Container layout onto the portal edit page.

6.  On the container, add a set of columns by selecting the plus icon \(\[Omitted image "circle-plus-outline-24.svg"\]\)

7.  On the Widgets pane, in the **Filter Widget** field, enter the Widget name.

8.  Drag the widget onto the container.

9.  Select **Save**.


## Result

The widget is added to the page. Adding a widget to a page creates a new Widget Instance that can be modified separately, and changes will appear on that page **only**. For information on how to add portal widgets to page\(s\), see [Configure the GOV.UK Design System Service Portal Pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-pages.md).

**Parent Topic:**[Configure the GOV.UK Design System Service Portal Widgets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-widgets.md)

