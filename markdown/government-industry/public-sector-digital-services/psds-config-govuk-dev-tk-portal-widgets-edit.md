---
title: Customize Widgets for GOV.UK Design System Service Portal pages
description: You can use base system widgets as-is in the GDS Service Portal, or you may clone them to suit your needs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-widgets-edit.html
release: australia
product: Public Sector Digital Services
classification: public-sector-digital-services
topic_type: task
last_updated: "2026-06-02"
reading_time_minutes: 2
breadcrumb: [Configure widgets, Configure UK GDS Service Portal, GOV.UK Developer Toolkit, Set up self-service, Configure, Public Sector Digital Services \(PSDS\)]
---

# Customize Widgets for GOV.UK Design System Service Portal pages

You can use base system widgets as-is in the GDS Service Portal, or you may clone them to suit your needs.

## Before you begin

Role required: admin

## About this task

By default, the GOV.UK Developer Toolkit provides you with a library of reusable portal widgets that follow UK GDS guidelines. Base system widgets are read-only so you can benefit from future updates. To make changes, you can clone base system widgets.

**Note:** Cloned widgets are considered custom and don't benefit from future updates to the widgets they were cloned from. To learn more about cloning or creating widgets, see Developing custom widgets.

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Service Portal Configuration**.

2.  Open the **Widget Editor**, then select an existing widget from the **Select a widget** list.

    For example, select **Error Widget**.

    **Note:** Base system widgets are read-only so you can benefit from future updates. To make changes, you can clone base system widgets. However, cloned widgets are considered custom and don't benefit from future updates to the widgets they were cloned from.

3.  From the list menu in the widget header, select **Clone \[Widget Name\]**.

    For example, select **Clone Error Widget**.

4.  Enter a name for the cloned widget.

    The widget ID is created automatically based on the widget name.

5.  **Optional**: Select **Create test page** to automatically create a page containing the widget.

6.  Use the check boxes to show or hide the different components of the widget editor as needed.

7.  Make changes to the HTML Template, CSS, client script, server script, or the link function.

    **Note:** For server-side scripts, you can turn on using the ECMAScript 2021 \(ES12\) JavaScript mode if your application uses ES5 Standards mode or Compatibility mode. Scripts in applications with the JavaScript mode set to ECMAScript 2021 \(ES12\) use ECMAScript 2021 \(ES12\) by default. For more information, see Turn on ECMAScript 2021 \(ES12\) mode for a script.

8.  To enable a preview of your widget, select the eye icon from the menu bar to **Enable Preview**.

9.  Select **Save**.

    **Note:** If you clone a widget that uses the Angular ng-template, you must manually clone the template and change the name of the template reference in the widget.


## Result

The cloned widget is created and can be added to any page that has been created in the portal. Adding a widget to a page creates a new Widget Instance that can be modified separately, and changes will appear on that page **only**. For information on how to add portal widgets to page\(s\), see [Configure the GOV.UK Design System Service Portal Pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-pages.md).

**Parent Topic:**[Configure the GOV.UK Design System Service Portal Widgets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-widgets.md)

