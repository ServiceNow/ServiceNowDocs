---
title: Add a dashboard to a Dashboards page
description: You can add either a technical dashboard or one made in the inline editor to a page you built from the Dashboards page template. Configure the dashboard component on that page.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Creating Platform Analytics pages, Platform Analytics experience, Platform Analytics]
---

# Add a dashboard to a Dashboards page

You can add either a technical dashboard or one made in the inline editor to a page you built from the Dashboards page template. Configure the dashboard component on that page.

## Before you begin

Role required: ui\_builder\_admin

## About this task

To add a dashboard to a page in UI Builder, create the page from the Dashboards page template, as described in [Add Platform Analytics pages to a configurable workspace](add-analytics-center-to-experience.md#). You can then either populate the dashboard in the inline editor or expose an existing dashboard. The existing dashboard can be either a technical dashboard or one created in the inline editor. You can expose an entire dashboard or only selected tabs.

## Procedure

1.  If there is an existing dashboard that you want to show in your experience, add your experience or configurable workspace to the **Dashboard visibility** field in the details of that dashboard.

    Dashboard details are available through the inline editor, even for technical dashboards. For more information, see [Configure Platform Analytics dashboard details](../../dashboards/task/config-db-in-ac.md).

    **Note:** Ignore this step if there is no existing dashboard that you want to show.

2.  Navigate to **All** &gt; **Experiences** and open your workspace.

3.  Create a page in the workspace using the Dashboards page template, or open an existing page created from the template.

    For more information, see [Create a page from a template](https://www.servicenow.com/docs/access?context=reuse-page-definitions&version=zurich&pubname=zurich-application-development&ft:locale=en-US) and [Add Platform Analytics pages to a configurable workspace](add-analytics-center-to-experience.md#).

    **Note:** You cannot add a Dashboard component to a page. You can only create a page from the Dashboards template. This page will include a Dashboard component.

    You now have an inline dashboard editor that you or another user can open by navigating to this page.

4.  Open the Dashboard component on the page and go to the configuration panel.

    If you want this page to display an existing dashboard, continue to the next step. If you want this page to open on an empty inline dashboard editor, skip to Step [7](add-dashboard-to-workspace.md#step_use-as-embedded).

5.  In **Default dashboard**, select the dashboard that you want to add to the page.

    -   If there is one specific dashboard you want to show, select it from the dropdown list. If your dashboard is not listed, be sure it is visible in this workspace or experience as described in Step 1.
    -   If you want different dashboards to be displayed according to choices that the viewer makes on the page, use data binding to select the dashboard according to a @state variable.
    -   For other ways to select the dashboard dynamically, write a script.
    **Note:** If you select a dashboard that was created in the inline editor, filters on that dashboard retain their values across logins or page refreshes unless the filter configuration is edited.

6.  If you only want to show a specific tab of the imported dashboard, specify the **Tab SysId**.

    Like with the dashboard itself, you can specify a tab or have it selected dynamically through data binding or scripting.

7.  Select **Use as embedded** if you want to use the dashboard component inside your page in isolation from the page's URL parameters.

    In other words, turn on for full control over what the dashboard renders, regardless of URL parameters. The Copy URL and Copy URL with filter options are not available on such embedded dashboards.

8.  Set the other configuration options as they are described in [Dashboard component properties](../../../build/component-uib-setup/reference/dashboard-component-properties-setup.md).


## What to do next

You can open the dashboard in runtime and edit it in the inline editor. Any viewer with edit rights can do the same. If the viewer has the rights to save a dashboard to the library, they have the option of saving the dashboard locally or altering the original dashboard in the library in Platform Analytics.

-   **[Dashboard component properties](../../../build/component-uib-setup/reference/dashboard-component-properties-setup.md)**  
Disable and enable dashboard component runtime user abilities with these properties.
-   **[Dashboard component events](../../../build/component-uib-setup/reference/dashboard-component-events-setup.md)**  
Select event handlers to configure the actions \(events\) provided with the dashboard component.

**Parent Topic:**[Creating Platform Analytics pages in your own workspace](../concept/adding-analytics-center-to-ws.md)

**Related topics**  


[Create a Platform Analytics workspace from App Engine Studio](../concept/create-analytics-ws-aes.md)

[Add Platform Analytics pages to a configurable workspace](add-analytics-center-to-experience.md#)

[Configure custom redirection from a dashboard component](config-custom-redirection-from-db.md)

[Pass global filters to the dashboard page template](../../par-for-workspace/task/pass-global-filters-to-db.md)

[Configure dashboard data broker](../../../build/component-uib-setup/task/configure-dashboard-data-broker.md)

