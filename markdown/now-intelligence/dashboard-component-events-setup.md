---
title: Dashboard component events
description: Select event handlers to configure the actions \(events\) provided with the dashboard component.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Add a dashboard to a page, Creating Platform Analytics pages, Platform Analytics experience, Platform Analytics]
---

# Dashboard component events

Select event handlers to configure the actions \(events\) provided with the dashboard component.

The Events tab shows the events used by the dashboard component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

## Event handlers

Event handlers work with data resources to link the dashboard actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

## Event descriptions

<table id="table_j4k_dw5_c5b"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Navigate to dashboard overview page

</td><td>

Dispatched when the dashboard is closed and redirects to the dashboard library. You can customize this behavior by changing the route and title in the Redirect to dashboard list client script. To open client scripts, select the &lt;&gt; icon in the page's side bar.```javascript
* @param {params} params
* @param {api} params.api
* @param {any} params.event
* @param {any} params.imports
* @param {ApiHelpers} params.helpers
*/
function handler({api}) {
    api.emit('SCREEN_STATUS_CHANGED', {status: 'closed'});
    api.emit('NAV_ITEM_SELECTED', {
        route: 'dashboard-library',
        title: 'Dashboard Library',
    });
}
```

</td></tr><tr><td>

Dashboard Widget Clicked

</td><td>

Add this event handler if you want to override the default drilldown with custom behavior when a visualization on the dashboard is clicked. It uses the Dashboard Widget Clicked client script. To add a custom drilldown:

1.  Set the defaultDrilldowns property to false.
2.  Add the Dashboard Widget Clicked event handler.
3.  Open the Dashboard Widget Clicked client script. To open client scripts, select the &lt;&gt; icon in the page's side bar.
4.  Locate the code `api.emit('NAV_ITEM_SELECTED', payload);` and update `payload` to align with your custom redirect logic.

</td></tr><tr><td>

URL params update requested

</td><td>

Dispatched whenever the dashboard component would normally update URL parameters and **delegateUrlParams** is `true`. This event provides structured parameter data that client scripts can use to implement custom navigation logic.

 URL parameters:

-   sysId: The sys\_id of the dashboard being navigated to. Present when dashboard changes.
-   tabSysId: The sys\_id of the selected tab. Present when tab changes.
-   edit: Whether the dashboard is in edit mode. Present when edit mode changes.

 All parameters have the following object fields:

-   value \(string \| boolean\): The parameter value
-   description \(string\): Human-readable description of the parameter

 The sysId parameter also has the following object fields:

-   dashboardName \(string\): Title of the dashboard
-   isNewTab \(boolean\): `true` when the user performed a Cmd/Ctrl+click or middle-click in the dashboard picker, indicating intent to open in a new tab. Only sent for `sysId` parameter.

 Example:

```json
{
  "urlParams": {
    "sysId": {
      "value": "a1b2c3d4e5f6",
      "dashboardName": "Dashboard A",
      "description": "Dashboard sys_id",
      "isNewTab": false
    },
    "tabSysId": {
      "value": "f6e5d4c3b2a1",
      "description": "Tab sys_id"
    },
    "edit": {
      "value": true,
      "description": "Edit mode"
    }
  }
}
```

 For more information, see [Dashboard URL parameter delegation](../concept/dashboard-url-parameter-delegation.md#).

**Note:** This functionality requires the latest Platform Analytics experience application from the ServiceNow® Store.

</td></tr></tbody>
</table>**Parent Topic:**[Add a dashboard to a Dashboards page](../../../use/performance-analytics/task/add-dashboard-to-workspace.md)

