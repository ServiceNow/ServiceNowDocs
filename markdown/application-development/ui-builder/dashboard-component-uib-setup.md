---
title: Dashboard component setup
description: The Dashboard component provides an inline editor for users to create dashboards in runtime. This component replaces the Dashboard viewport component that was deprecated in the Tokyo release. Pages that previously used Dashboard viewport are automatically updated to use Dashboard.Disable and enable dashboard component runtime user abilities with these properties.Select event handlers to configure the actions \(events\) provided with the dashboard component.The Delegate URL params property enables UIB pages containing dashboard components to control how URL parameter updates are handled. Doing so enables custom navigation logic for embedded or workspace scenarios.Enable URL parameter delegation for dashboard components to implement custom navigation logic in UIB pages.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/dashboard-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 12
keywords: [dashboard, URL parameters, UIB, delegation, dashboard, URL parameters, UIB, configuration]
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Dashboard component setup

The Dashboard component provides an inline editor for users to create dashboards in runtime. This component replaces the Dashboard viewport component that was deprecated in the Tokyo release. Pages that previously used Dashboard viewport are automatically updated to use Dashboard.

## Before you begin

The Dashboard component is only available on pages you create using the Dashboards page template. You cannot add the component to a page.

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

The dashboard includes a Dashboard data broker preset. This data broker prefetches all the static JavaScript assets that are required by the visualizations that are rendered in the dashboard. This prefetch could speed the loading of visualizations that include many such assets.

The preset includes a data controller \(or broker\). After you activate the preset, bind the properties of the controller to the correct page properties. For more information, see [Configure dashboard data broker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/configure-dashboard-data-broker.md).

**Warning:** Activating the data broker resets any configuration options you have set back to default values. Note any configurations you have set before you activate the preset, so you can restore them later.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for Dashboard that differentiates it from other components in the content tree.

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

2.  Select the Dashboard component using one of these methods:

    -   Click anywhere within the component on the page.
    -   Select the label you created for your component in the content tree.
    The configuration options appear in the panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Dashboard component properties

Disable and enable dashboard component runtime user abilities with these properties.

<table id="table_omt_qqt_c5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Tab Sys Id \[tabSysId\]

</td><td>

If you want to display only one tab of an existing dashboard, specify its SysID. Also specify the dashboard in Default dashboard.You can select a dashboard statically or dynamically, through a state variable or a script.

</td></tr><tr><td>

Use default redirections \[defaultDrilldowns\]

</td><td>

When activated, the inline editor adds default pre-configured redirections for when a segment of a data visualization is clicked. To implement a custom drilldown, set this property to false, then add and customize a Dashboard Widget Clicked event handler as described in the Events section. Default: true

</td></tr><tr><td>

Disable the whole header \[hideHeader\]

</td><td>

Viewers do not see the dashboard header, only the content.

</td></tr><tr><td>

Hide dashboard picker \[hideDashboardPicker\]

</td><td>

When true, hides the dashboard picker on all dashboards in the workspaceDefault: false

</td></tr><tr><td>

Picker Encoded Query \[pickerEncodedQuery\]

</td><td>

Limits the dashboards that the dashboard picker lists to those that match an encoded query for the `par_dashboard` table. The query applies in addition to workspace visibility and the viewer's permissions. Leave empty to list all the dashboards that the viewer can access.For more information, see .

Default: empty

</td></tr><tr><td>

Disable sharing \[hideShareButton\]

</td><td>

Hides the Share button on all dashboards from all users, but applies only to the Dashboards page where this value is set.Default: false

</td></tr><tr><td>

Disable editing \[hideEditButton\]

</td><td>

Hides the Edit button on all dashboards from all users, but applies only to the Dashboards page where this value is set.Default: false

</td></tr><tr><td>

Disable dashboard creation \[hideCreateNewButton\]

</td><td>

Hides the Create Dashboard option in the 3-dot menu of the Dashboard page. Users can still create dashboards from the Analytics Center or the dashboards library \(Dashboard Overview component\).When false:

 \[Omitted image "hide-create-dashboard-false.png"\] Alt text: 3-dot menu of dashboards when Disable dashboard creation is off.

 When true:

 \[Omitted image "hide-create-dashboard-true.png"\] Alt text: 3-dot menu of dashboard page when Disable dashboard creation is on.

 Default: false

</td></tr><tr><td>

Use as embedded \[useAsEmbedded\]

</td><td>

Set to true when you, as a developer, want to use the dashboard component inside your page in isolation from the page's URL parameters. Meaning, you want full control over what the dashboard renders, regardless of URL parameters. The Copy URL and Copy URL with filter options are not available on such embedded dashboards.Default: false

</td></tr><tr><td>

Delegate URL params \[delegateUrlParams\]

</td><td>

Allows the UIB pages which contains the dashboard to take control of how the Dashboard component handles URL parameter updates. When enabled, instead of the dashboard directly updating the browser URL, it dispatches a DASHBOARD\#URL\_PARAMS\_UPDATE\_REQUESTED event containing the parameters that would have been updated. The parent page can then handle navigation using a client script.Set this property in these circumstances:

-   The page URL structure does not include dashboard URL parameters \(for example, no sys-id in the URL path\).
-   The page needs custom navigation logic for dashboard changes.
-   The dashboard is embedded \(without isEmbedded turned on\) in a workspace where URL management is handled by the parent.

For more information, see [Dashboard URL parameter delegation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/dashboard-component-uib-setup.md).

</td></tr><tr><td>

Default dashboard \[defaultDashboard\]

</td><td>

Select an existing dashboard to show in this dashboard component. This other dashboard is usually in the Platform Analytics Experience. For that dashboard to be shown, it must include your workspace or experience in the **Dashboard Visibility** field in its dashboard details, as described in [Configure Platform Analytics dashboard details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/config-db-in-ac.md).You can select a dashboard statically or dynamically, through a state variable or a script.

</td></tr><tr><td>

Shareable Filter SysID \[filterId\]

</td><td>

The sysId of the persisted filter set up of a dashboard

</td></tr><tr><td>

Global filters \[globalFilters\]

</td><td>

Filters for the visualizations within the dashboard. These filters apply to all relevant data visualizations. The format of the value passed to globalFilter is the stringified form of \{encodedQueries: 'encoded-queries-string', filters: 'PAR-Filter'\}. Both encodedQueries and filters are transformed into PAR filters internally and merged with existing filters in the dashboard.Either `encodedQueries`, `filters`, or both can be specified. In the following example, equivalent `encodedQueries` and `filters` values both filter visualizations that show records from the Incident \[incident\] table based on a State field value of 1 or 2:

```
JSON.stringify({
    encodedQueries: {incident: 'stateIN1,2'},
    parFilters: [{ order: 0, apply_to: ['incident.state'], values: ['1', '2'] }]
})
```

</td></tr><tr><td>

Drilldown to Core UI \[drilldownToCoreUI\]

</td><td>

Toggle on for drill down on table data sources to redirect to the Core UI list of table records. When off, drilling down opens a Simple List component of the table records, if the workspace contains a simple list.Does not apply to technical dashboards. Data visualizations on technical dashboards have to have their Visualization Clicked event handlers configured for drilldowns.

Default: off

</td></tr><tr><td>

Use data broker to fetch data \[useDataBroker\]

</td><td>

When toggled on, the dashboard prefetches static JavaScript, such as dashboard metadata, using a data broker. The Dashboard data broker preset automatically toggles this property on. Without the preset, this property is off by default. For more information, see [Configure dashboard data broker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/configure-dashboard-data-broker.md).

</td></tr><tr><td>

Data broker response for the dashboard \[data\]

</td><td>

The response for the data broker when it is used. The Dashboard data broker preset automatically sets a JSON object for this property. You can override this value or set it manually without turning the preset on, if you absolutely need to.

</td></tr></tbody>
</table>## Dashboard component events

Select event handlers to configure the actions \(events\) provided with the dashboard component.

The Events tab shows the events used by the dashboard component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the dashboard actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

### Event descriptions

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

 For more information, see [Dashboard URL parameter delegation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/dashboard-component-uib-setup.md).

</td></tr></tbody>
</table>## Dashboard URL parameter delegation

The Delegate URL params property enables UIB pages containing dashboard components to control how URL parameter updates are handled. Doing so enables custom navigation logic for embedded or workspace scenarios.

By default, dashboard components automatically update the browser URL when users switch dashboards, change tabs, or toggle edit mode. This behavior works well for standard dashboard pages but may not suit all implementation scenarios.

The **Delegate URL params** property provides an alternative approach where the dashboard component dispatches events instead of directly updating URLs. This delegation mechanism allows parent pages to implement custom navigation logic.

For information about this property in the context of the Dashboard component configuration panel, see [Dashboard component properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/dashboard-component-uib-setup.md).

### When to use URL parameter delegation

URL parameter delegation is useful in these scenarios:

-   The page URL structure does not include dashboard URL parameters — for example, no `sys-id` in the URL path
-   The page requires custom navigation logic for dashboard changes
-   The dashboard is embedded in a workspace where URL management is handled by the parent component
-   Multiple dashboard components exist on the same page and need coordinated URL handling

### How delegation works

When **Delegate URL params** is disabled \(default behavior\):

1.  User performs an action, such as switching the dashboard, changing the tab, or toggling edit mode
2.  Dashboard component dispatches an internal `CONTENT_UPDATED` action
3.  UIB framework processes the action and updates URL parameters automatically

When **Delegate URL params** is enabled:

1.  User performs an action
2.  Dashboard component suppresses the `CONTENT_UPDATED` dispatch
3.  Dashboard component dispatches `DASHBOARD#URL_PARAMS_UPDATE_REQUESTED` with structured parameter data
4.  Client script on the page receives the event and implements custom navigation logic

### Event payload structure

The `DASHBOARD#URL_PARAMS_UPDATE_REQUESTED` event contains a **urlParams** object with structured parameter information. Each parameter includes the value, description, and additional metadata such as dashboard names and new tab indicators.

This structured approach provides client scripts with sufficient context to make informed navigation decisions, including handling special cases like opening dashboards in new browser tabs.

For more information about this event, see [Dashboard component events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/dashboard-component-uib-setup.md).

### Configure dashboard URL parameter delegation

Enable URL parameter delegation for dashboard components to implement custom navigation logic in UIB pages.

#### Before you begin

Role required: ui\_builder\_admin

#### About this task

Configure URL parameter delegation when you need custom control over how dashboard navigation updates browser URLs. This is useful for embedded dashboards, workspace scenarios, or pages with non-standard URL structures.

#### Procedure

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


#### Result

When users interact with the dashboard \(switch dashboards, change tabs, toggle edit mode\), the component dispatches events that your client script can handle with custom navigation logic.

#### Basic delegation client script

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

