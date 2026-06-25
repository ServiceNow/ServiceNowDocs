---
title: Configure custom redirection from a dashboard component
description: If you have created a page in your workspace from the Dashboard page template, you can customize the on-click redirection from the dashboard component on that page. The inline dashboard that this component displays will follow the custom redirection.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/config-custom-redirection-from-db.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Creating Platform Analytics pages, Platform Analytics experience, Platform Analytics]
---

# Configure custom redirection from a dashboard component

If you have created a page in your workspace from the Dashboard page template, you can customize the on-click redirection from the dashboard component on that page. The inline dashboard that this component displays will follow the custom redirection.

## Before you begin

You have created a workspace in UI Builder with a page generated from the Dashboard page template. You may also have set the dashboard component in that page to display a dashboard from the library as described in [Add a dashboard to a Dashboards page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/add-dashboard-to-workspace.md).

Role required: ui\_builder\_admin

## About this task

**Important:** The procedure described here applies only to dashboards created in the inline editor. For technical dashboards, you configure redirection through a drilldown event for each data visualization. For more information, see [Add a drilldown event to a data visualization on a technical dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/add-custom-drilldown-event.md).

## Procedure

1.  Open your workspace in UI Builder.

2.  Open the relevant page.

    You will have built this page using the Dashbords page template.

3.  Select the dashboard component.

4.  In the configuration panel, turn off **Use default redirections**.

    \[Omitted image "db-turnoff-redirections.png"\] Alt text: Turning off default redirections.

    You have turned off redirections. Clicking on a visualization at runtime does not trigger any actions.

5.  In the events panel, look whether there is a "Dashboard widget clicked" event handler.

6.  If there is no "Dashboard widget clicked" handler, add one.

    1.  Select **+ Add event mapping**.

    2.  From the list of available events, select Dashboard widget clicked.

        \[Omitted image "db-add-db-widget-clicked-event.png"\] Alt text: Selecting the Dashboard widget clicked event.

7.  In the Data and scripts area of the page, under Client scripts, open Dashboard Widget Clicked.

    \[Omitted image "db-dashboard-widget-clicked.png"\] Alt text: Opening the Dashboard widget clicked script in the editor.

8.  In the Edit client script pane, find the line `api.emit('NAV_ITEM_SELECTED', payload);`.

9.  Update the payload to align with your custom redirection logic.


## Result

All redirections from data visualizations on that dashboard open your specified target.

**Parent Topic:**[Creating Platform Analytics pages in your own workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/adding-analytics-center-to-ws.md)

**Related topics**  


[Create a Platform Analytics workspace from App Engine Studio]()

[Add Platform Analytics pages to a configurable workspace]()

[Add a dashboard to a Dashboards page]()

[Dashboard URL parameter delegation]()

[Pass global filters to the dashboard page template]()

[Configure dashboard data broker]()

