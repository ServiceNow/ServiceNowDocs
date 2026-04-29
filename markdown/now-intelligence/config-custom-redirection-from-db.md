---
title: Configure custom redirection from a dashboard component
description: If you have created a page in your workspace from the Dashboard page template, you can customize the on-click redirection from the dashboard component on that page. The inline dashboard that this component displays will follow the custom redirection.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Creating Platform Analytics pages, Platform Analytics experience, Platform Analytics]
---

# Configure custom redirection from a dashboard component

If you have created a page in your workspace from the Dashboard page template, you can customize the on-click redirection from the dashboard component on that page. The inline dashboard that this component displays will follow the custom redirection.

## Before you begin

You have created a workspace in UI Builder with a page generated from the Dashboard page template. You may also have set the dashboard component in that page to display a dashboard from the library as described in [Add a dashboard to a Dashboards page](add-dashboard-to-workspace.md).

Role required: ui\_builder\_admin

## About this task

**Important:** The procedure described here applies only to dashboards created in the inline editor. For technical dashboards, you configure redirection through a drilldown event for each data visualization. For more information, see [Add a drilldown event to a data visualization on a technical dashboard](../../dashboards/task/add-custom-drilldown-event.md).

## Procedure

1.  Open your workspace in UI Builder.

2.  Open the relevant page.

    You will have built this page using the Dashbords page template.

3.  Select the dashboard component.

4.  In the configuration panel, turn off **Use default redirections**.

    ![Turning off default redirections.](../../par-for-workspace/image/db-turnoff-redirections.png)

    You have turned off redirections. Clicking on a visualization at runtime does not trigger any actions.

5.  In the events panel, look whether there is a "Dashboard widget clicked" event handler.

6.  If there is no "Dashboard widget clicked" handler, add one.

    1.  Select **+ Add event mapping**.

    2.  From the list of available events, select Dashboard widget clicked.

        ![Selecting the Dashboard widget clicked event.](../../par-for-workspace/image/db-add-db-widget-clicked-event.png)

7.  In the Data and scripts area of the page, under Client scripts, open Dashboard Widget Clicked.

    ![Opening the Dashboard widget clicked script in the editor.](../../par-for-workspace/image/db-dashboard-widget-clicked.png)

8.  In the Edit client script pane, find the line `api.emit('NAV_ITEM_SELECTED', payload);`.

9.  Update the payload to align with your custom redirection logic.


## Result

All redirections from data visualizations on that dashboard open your specified target.

**Parent Topic:**[Creating Platform Analytics pages in your own workspace](../concept/adding-analytics-center-to-ws.md)

**Related topics**  


[Create a Platform Analytics workspace from App Engine Studio](../concept/create-analytics-ws-aes.md)

[Add Platform Analytics pages to a configurable workspace](add-analytics-center-to-experience.md#)

[Add a dashboard to a Dashboards page](add-dashboard-to-workspace.md)

[Dashboard URL parameter delegation](../../../build/component-uib-setup/concept/dashboard-url-parameter-delegation.md#)

[Pass global filters to the dashboard page template](../../par-for-workspace/task/pass-global-filters-to-db.md)

[Configure dashboard data broker](../../../build/component-uib-setup/task/configure-dashboard-data-broker.md)

