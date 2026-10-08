---
title: Add a step-by-step navigation widget to a GOV.UK Design System Service Portal page
description: You can use base system widgets as-is in the GDS Service Portal, or you may clone them to suit your needs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/psds-config-govuk-dev-tk-step-by-step-nav-edit.html
release: brazil
topic_type: task
last_updated: "2026-06-02"
reading_time_minutes: 2
breadcrumb: [Add widgets to portal pages, Configure widgets, Configure UK GDS Service Portal, GOV.UK Developer Toolkit, Set up self-service, Configure, Public Sector Digital Services \(PSDS\)]
---

# Add a step-by-step navigation widget to a GOV.UK Design System Service Portal page

You can use base system widgets as-is in the GDS Service Portal, or you may clone them to suit your needs.

## Before you begin

Role required: admin

## About this task

Step-by-step navigation is a full, deliberately-built pattern implementation with two cooperating widgets, the UK GDS Step-by-Step \(uk-gds-step-by-step\) widget, and the optional UK GDS Task List widget \(uk-gds-task-list\) that shows task progress. The GOV.UK Developer Toolkit step-by-step navigation follows the GOV.UK step-by-step navigation pattern guidelines — numbered, collapsible steps, each with one or more task that links out to a question-page journey, record producer, portal page, KB article, external service, or offline action. This navigation can be hosted on a sidebar or directly on a landing page, and shows task order or status, depending on the widget configured.

The Step-by-step navigation page pattern widgets can be viewed and cloned from the default page for `uk_gds_missed_waste`. You can clone and copy the page and all its components, then customize it to fit your needs.

**Note:** Cloned widgets are considered custom and don't benefit from future updates to the widgets they were cloned from. To learn more about cloning or creating widgets, see [Developing custom widgets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-user-interface/widget-dev-guide.md).

## Procedure

1.  Navigate to **All**.

2.  Run script:

    ```
    npx now-sdk build
    npx now-sdk install --demoData
    ```

3.  Verify the post-install correction ran by checking the system log for `[UK GDS fix] done` before continuing.

4.  Open the **Widget Editor**, then select an existing widget from the **Select a widget** list.

    For example, select **Error Widget**.

    **Note:** 

5.  From the list menu in the widget header, select **Clone \[Widget Name\]**.

    For example, select **Clone Error Widget**.

6.  Enter a name for the cloned widget.

    The widget ID is created automatically based on the widget name.

7.  **Optional**: Select **Create test page** to automatically create a page containing the widget.

8.  Use the check boxes to show or hide the different components of the widget editor as needed.

9.  Make changes to the HTML Template, CSS, client script, server script, or the link function.

    **Note:** For server-side scripts, you can turn on using the ECMAScript 2021 \(ES12\) JavaScript mode if your application uses ES5 Standards mode or Compatibility mode. Scripts in applications with the JavaScript mode set to ECMAScript 2021 \(ES12\) use ECMAScript 2021 \(ES12\) by default. For more information, see Turn on ECMAScript 2021 \(ES12\) mode for a script.

10. To enable a preview of your widget, select the eye icon from the menu bar to **Enable Preview**.

11. Select **Save**.

    **Note:** If you clone a widget that uses the Angular ng-template, you must manually clone the template and change the name of the template reference in the widget.


## Result

The cloned widget is created and can be added to any page that has been created in the portal. Adding a widget to a page creates a new Widget Instance that can be modified separately, and changes will appear on that page **only**. For information on how to add portal widgets to page\(s\), see [Configure the GOV.UK Design System Service Portal Pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/government-industry/psds-config-govuk-dev-tk-portal-pages.md).

