---
title: Dashboard URL parameter delegation
description: The Delegate URL params property enables UIB pages containing dashboard components to control how URL parameter updates are handled. Doing so enables custom navigation logic for embedded or workspace scenarios.Enable URL parameter delegation for dashboard components to implement custom navigation logic in UIB pages.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-31"
reading_time_minutes: 4
keywords: [dashboard, URL parameters, UIB, delegation, dashboard, URL parameters, UIB, configuration]
breadcrumb: [Creating Platform Analytics pages, Platform Analytics experience, Platform Analytics]
---

# Dashboard URL parameter delegation

The Delegate URL params property enables UIB pages containing dashboard components to control how URL parameter updates are handled. Doing so enables custom navigation logic for embedded or workspace scenarios.

**Note:** This functionality requires the latest Platform Analytics experience application from the ServiceNow® Store.

By default, dashboard components automatically update the browser URL when users switch dashboards, change tabs, or toggle edit mode. This behavior works well for standard dashboard pages but may not suit all implementation scenarios.

The **Delegate URL params** property provides an alternative approach where the dashboard component dispatches events instead of directly updating URLs. This delegation mechanism allows parent pages to implement custom navigation logic.

For information about this property in the context of the Dashboard component configuration panel, see [Dashboard component properties](../reference/dashboard-component-properties-setup.md).

## When to use URL parameter delegation

URL parameter delegation is useful in these scenarios:

-   The page URL structure does not include dashboard URL parameters — for example, no `sys-id` in the URL path
-   The page requires custom navigation logic for dashboard changes
-   The dashboard is embedded in a workspace where URL management is handled by the parent component
-   Multiple dashboard components exist on the same page and need coordinated URL handling

## How delegation works

When **Delegate URL params** is disabled \(default behavior\):

1.  User performs an action, such as switching the dashboard, changing the tab, or toggling edit mode
2.  Dashboard component dispatches an internal `CONTENT_UPDATED` action
3.  UIB framework processes the action and updates URL parameters automatically

When **Delegate URL params** is enabled:

1.  User performs an action
2.  Dashboard component suppresses the `CONTENT_UPDATED` dispatch
3.  Dashboard component dispatches `DASHBOARD#URL_PARAMS_UPDATE_REQUESTED` with structured parameter data
4.  Client script on the page receives the event and implements custom navigation logic

## Event payload structure

The `DASHBOARD#URL_PARAMS_UPDATE_REQUESTED` event contains a **urlParams** object with structured parameter information. Each parameter includes the value, description, and additional metadata such as dashboard names and new tab indicators.

This structured approach provides client scripts with sufficient context to make informed navigation decisions, including handling special cases like opening dashboards in new browser tabs.

For more information about this event, see [Dashboard component events](../reference/dashboard-component-events-setup.md).

**Parent Topic:**[Creating Platform Analytics pages in your own workspace](../../../use/performance-analytics/concept/adding-analytics-center-to-ws.md)

**Related topics**  


[Create a Platform Analytics workspace from App Engine Studio](../../../use/performance-analytics/concept/create-analytics-ws-aes.md)

[Add Platform Analytics pages to a configurable workspace](../../../use/performance-analytics/task/add-analytics-center-to-experience.md#)

[Add a dashboard to a Dashboards page](../../../use/performance-analytics/task/add-dashboard-to-workspace.md)

[Configure custom redirection from a dashboard component](../../../use/performance-analytics/task/config-custom-redirection-from-db.md)

[Pass global filters to the dashboard page template](../../../use/par-for-workspace/task/pass-global-filters-to-db.md)

[Configure dashboard data broker](../task/configure-dashboard-data-broker.md)

## Configure dashboard URL parameter delegation

Enable URL parameter delegation for dashboard components to implement custom navigation logic in UIB pages.

### Before you begin

Role required: ui\_builder\_admin

### About this task

Configure URL parameter delegation when you need custom control over how dashboard navigation updates browser URLs. This is useful for embedded dashboards, workspace scenarios, or pages with non-standard URL structures.

### Procedure

1.  Navigate to the UIB page containing the dashboard component.

2.  Select the dashboard component in the design canvas.

3.  Open the **Configure** tab in the component properties panel.

4.  Select the **Delegate URL params** check box.

    When enabled, the dashboard component will dispatch `DASHBOARD#URL_PARAMS_UPDATE_REQUESTED` events instead of updating URLs directly.

5.  Switch to the **Events** tab.

6.  Select **Add event mapping**.

7.  Select the **URL params update requested** event from the list.

8.  Add an event handler that executes a client script.

    The client script will receive the URL parameter data and implement your custom navigation logic.

9.  Create a client script to handle the URL parameter updates.

    The script receives a structured **urlParams** payload containing parameter values, descriptions, and metadata such as dashboard names and new tab indicators.

    The dashboard component now delegates URL parameter handling to your custom client script instead of updating the browser URL directly.


### Result

When users interact with the dashboard \(switch dashboards, change tabs, toggle edit mode\), the component dispatches events that your client script can handle with custom navigation logic.

### Basic delegation client script

This example script replicates the default URL update behavior:

```javascript
function handler({api, event}) {
    const {urlParams} = event.payload;
    
    for (const [key, paramInfo] of Object.entries(urlParams)) {
        if (key === 'sysId' && paramInfo.isNewTab === true) {
            // Handle new tab navigation
            api.emit('NAV_ITEM_SELECTED', {
                route: 'dashboards',
                title: paramInfo.dashboardName || paramInfo.value,
                params: {sysId: paramInfo.value},
                navigationOptions: {
                    navigateExternal: true,
                    target: '_blank'
                }
            });
            return;
        }
        
        // Handle normal navigation
        api.emit('CONTENT_UPDATED', {
            route: 'dashboards',
            params: {[key]: paramInfo.value}
        });
    }
}
```

