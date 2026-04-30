---
title: Dashboard component properties
description: Disable and enable dashboard component runtime user abilities with these properties.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Add a dashboard to a page, Creating Platform Analytics pages, Platform Analytics experience, Platform Analytics]
---

# Dashboard component properties

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

Hides the Create New Dashboard option in the context menu of the Dashboard page. Users can still create dashboards from the Analytics Center or the dashboards library \(Dashboard Overview component\).When false:

 ![Context menu of dashboards when Disable dashboard creation is off.](../image/hide-create-dashboard-false.png)

 When true:

 ![Context menu of dashboard page when Disable dashboard creation is on.](../image/hide-create-dashboard-true.png)

 Default: false

</td></tr><tr><td>

Use as embedded \[useAsEmbedded\]

</td><td>

Set to true when you, as a developer, want to use the dashboard component inside your page in isolation from the page's URL parameters. Meaning, you want full control over what the dashboard renders, regardless of URL parameters. The Copy URL and Copy URL with filter options are not available on such embedded dashboards.Default: false

</td></tr><tr><td>

Default dashboard \[defaultDashboard\]

</td><td>

Select an existing dashboard to show in this dashboard component. This other dashboard is usually in the Platform Analytics Experience. For that dashboard to be shown, it must include your workspace or experience in the **Dashboard Visibility** field in its dashboard details, as described in [Configure Platform Analytics dashboard details](../../../use/dashboards/task/config-db-in-ac.md).You can select a dashboard statically or dynamically, through a state variable or a script.

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

When toggled on, the dashboard prefetches static JavaScript, such as dashboard metadata, using a data broker. The Dashboard data broker preset automatically toggles this property on. Without the preset, this property is off by default. For more information, see [Configure dashboard data broker](../task/configure-dashboard-data-broker.md).

</td></tr><tr><td>

Data broker response for the dashboard \[data\]

</td><td>

The response for the data broker when it is used. The Dashboard data broker preset automatically sets a JSON object for this property. You can override this value or set it manually without turning the preset on, if you absolutely need to.

</td></tr></tbody>
</table>**Parent Topic:**[Add a dashboard to a Dashboards page](../../../use/performance-analytics/task/add-dashboard-to-workspace.md)

