---
title: Dashboard API - ServiceNow Fluent
description: The Dashboard API defines dashboards \[par\_dashboard\] for organizing and sharing data visually.Create a shareable dashboard \[par\_dashboard\] with data visualizations, filters, tabs, widgets, permissions, and visibility rules.Create tabs \[par\_dashboard\_tab\] that contain widgets for a dashboard.Create widgets \[par\_dashboard\_widget\] within a tab in a grid layout.Configure the properties of widgets \[par\_dashboard\_widget\].Define permissions \[par\_dashboard\_permission\] to read, edit, and share a dashboard.Define visibility rules \[par\_dashboard\_visibility\] for which UX experiences display the dashboard.
locale: en-US
release: xanadu
product: ServiceNow SDK
classification: servicenow-sdk
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 11
keywords: [servicenow fluent, fluent api, servicenow fluent, fluent api, servicenow fluent, fluent api, servicenow fluent, fluent api, servicenow fluent, fluent api, servicenow fluent, fluent api, servicenow fluent, fluent api]
breadcrumb: [ServiceNow Fluent API reference, Reference, ServiceNow SDK, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Dashboard API - ServiceNow Fluent

The Dashboard API defines dashboards \[par\_dashboard\] for organizing and sharing data visually.

A dashboard consists of tabs, widgets, visibilities, and permissions. Each tab contains widgets that display data visualizations, headings, rich text, and other components.

Dashboards can be used as the home page of a workspace by referring to one or more workspaces from the visibilities array of the Dashboard object. To create a workspace, see [Workspace API - ServiceNow Fluent](fluent-workspace-api.md#).

For general information about dashboards, see [Dashboards in Platform Analytics](https://www.servicenow.com/docs/access?context=analytics-center-dashboards&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US).

**Parent Topic:**[ServiceNow Fluent API reference](servicenow-fluent-api-reference.md)

**Related topics**  


[ServiceNow Fluent](../concept/servicenow-fluent.md)

## Dashboard object

Create a shareable dashboard \[par\_dashboard\] with data visualizations, filters, tabs, widgets, permissions, and visibility rules.

<table id="table_i5f_wpy_23c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

$id

</td><td>

String or Number

</td><td>

Required. A unique ID for the metadata object. When you build the application, this ID is hashed into a unique sys\_id. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).Format: `Now.ID['String' or Number]`

</td></tr><tr><td>

name

</td><td>

String

</td><td>

Required. A name to display for the dashboard.

</td></tr><tr><td>

active

</td><td>

Boolean

</td><td>

Flag that indicates whether the dashboard is active.Default: true

</td></tr><tr><td>

tabs

</td><td>

Array

</td><td>

A list of tabs to display in the dashboard. For more information, see [tabs array](fluent-dashboard-api.md#).

</td></tr><tr><td>

permissions

</td><td>

Array

</td><td>

A list of user permissions required to access the dashboard. For more information, see [permissions array](fluent-dashboard-api.md#).

</td></tr><tr><td>

visibilities

</td><td>

Array

</td><td>

A list of visibility rules that control which UX experiences display the dashboard. For more information, see [visibilities array](fluent-dashboard-api.md#).Default: A default visibility rule with sys\_id 08c73d60537101100834ddeeff7b1287 is used.

</td></tr><tr><td>

$meta

</td><td>

Object

</td><td>

Metadata for the application metadata.With the installMethod property, you can map the application metadata to an output directory that loads only in specific circumstances.

```javascript
$meta: {
      installMethod: 'String'
}
```

Valid values for installMethod:

-   demo: Outputs the application metadata to the `metadata/unload.demo` directory to be installed with the application when the **Load demo data** option is selected.
-   first install: Outputs the application metadata to the `metadata/unload` directory to be installed only the first time an application is installed on an instance.

</td></tr></tbody>
</table>```javascript
import { Dashboard } from '@servicenow/sdk/core'

Dashboard({
    $id: Now.ID['incident-dashboard'],
    name: 'Incident Management Dashboard',
    tabs: [
        {
            $id: Now.ID['overview'],
            name: 'Overview',
            widgets: [
                {
                    $id: Now.ID['incident-count-chart'],
                    component: 'vertical-bar', // Vertical bar chart
                    componentProps: {
                        title: 'Incident Count',
                        dataSource: 'incident',
                        aggregation: 'count'
                    },
                    height: 8,
                    width: 6,
                    position: { x: 0, y: 0 },
                },
                {
                    $id: Now.ID['recent-incidents-list'],
                    component: 'list', // List component
                    componentProps: {
                        table: 'incident',
                        filter: 'active=true',
                        limit: 10,
                        columns: ['number', 'short_description', 'priority', 'state']
                    },
                    height: 8,
                    width: 6,
                    position: { x: 6, y: 0 },
                }
            ],
        },
        {
            $id: Now.ID['analytics'],
            name: 'Analytics',
            widgets: [
                {
                    $id: Now.ID['metrics-widget'],
                    component: 'single-score', // Single score component
                    componentProps: {
                        title: 'Key Metrics',
                        scoreSize: 'large'
                    },
                    height: 12,
                    width: 12,
                    position: { x: 0, y: 0 },
                }
            ],
        }
    ],
    permissions: [
        {
            $id: Now.ID['admin-user-permission'],
            user: '6816f79cc0a8016401c5a33be04be441', // sys_id of admin user
            canRead: true,
            canWrite: true,
            canShare: true,
            owner: true,
        },
        {
            $id: Now.ID['itil-role-permission'],
            role: '2831a114c611228501d4ea6c309d626d', // sys_id of itil role
            canRead: true,
        },
        {
            $id: Now.ID['support-group-permission'],
            group: '287ebd7da9fe198100f92cc8d1d2154e', // sys_id of IT Support group
            canRead: true,
        }
    ],
    visibilities: [
        {
            $id: Now.ID['workspace-visibility'],
            experience: myWorkspace,
        }
    ]
})
```

The workspace referenced is defined using the Workspace object:

```javascript
export const myWorkspace = Workspace({
  $id: Now.ID["my_workspace"],
  title: "My Workspace",
  path: "my-workspace",
  tables: ["incident"],
  listConfig: myListConfig
})
```

## tabs array

Create tabs \[par\_dashboard\_tab\] that contain widgets for a dashboard.

<table id="table_j3p_yqy_23c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

$id

</td><td>

String or Number

</td><td>

Required. A unique ID for the metadata object. When you build the application, this ID is hashed into a unique sys\_id. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).Format: `Now.ID['String' or Number]`

</td></tr><tr><td>

name

</td><td>

String

</td><td>

Required. A name to display on the tab.

</td></tr><tr><td>

active

</td><td>

Boolean

</td><td>

Flag that indicates whether the tab is active.Default: true

</td></tr><tr><td>

widgets

</td><td>

Array

</td><td>

A list of widgets to display in the tab. For more information, see [widgets array](fluent-dashboard-api.md#).

</td></tr></tbody>
</table>Within a dashboard, tabs are ordered using their position in the array.

```javascript
tabs: [
        {
            $id: Now.ID['overview-tab'],
            name: 'Overview',
            widgets: [
                {
                    $id: Now.ID['chart-widget'],
                    component: 'line', // Line chart component
                    componentProps: {
                        selectedElements: [],
                        chartVariation: 'stacked',
                        yAxisPosition: 'bottom'
                    },
                    height: 12,
                    width: 12,
                    position: { x: 0, y: 0 },
                },
                {
                    $id: Now.ID['header-widget'],
                    component: 'heading', // Heading component
                    componentProps: {
                        variant: 'header-primary',
                        label: 'Dashboard Metrics',
                        level: '1'
                    },
                    height: 4,
                    width: 12,
                    position: { x: 0, y: 12 },
                }
            ],
        },
        {
            $id: Now.ID['details-tab'],
            name: 'Details',
            widgets: []
        }
]
```

### widgets array

Create widgets \[par\_dashboard\_widget\] within a tab in a grid layout.

Dashboards use a 48-point grid system for positioning widgets.

<table id="table_jgr_d1z_23c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

$id

</td><td>

String or Number

</td><td>

Required. A unique ID for the metadata object. When you build the application, this ID is hashed into a unique sys\_id. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).Format: `Now.ID['String' or Number]`

</td></tr><tr><td>

component

</td><td>

Reference or String

</td><td>

Required. The name of a component \(such as line or single-score\) or the sys\_id of a component from the UX Macroponent Definition \[sys\_ux\_macroponent\] table to display as a widget.Component names aren't case sensitive and resolve to their sys\_ids during the build process.

</td></tr><tr><td>

height

</td><td>

Number

</td><td>

Required. The height of the widget in grid units.

</td></tr><tr><td>

width

</td><td>

Number

</td><td>

Required. The width of the widget in grid units.Maximum value: 48

</td></tr><tr><td>

position

</td><td>

Object

</td><td>

Required. The position of the widget in the grid layout with `x` and `y` properties. For example, a value of `{ x: 0, y: 0 }` positions the widget in the top-left corner of the grid.

</td></tr><tr><td>

componentProps

</td><td>

Object

</td><td>

The property configuration of a component. For more information, see [componentProps object](fluent-dashboard-api.md#).

</td></tr></tbody>
</table>```javascript
widgets: [
              {
                  $id: Now.ID['incident-count-chart'],
                  component: 'vertical-bar', // Vertical bar chart
                  componentProps: {
                      title: 'Incident Count',
                      dataSource: 'incident',
                      aggregation: 'count'
                  },
                  height: 8,
                  width: 6,
                  position: { x: 0, y: 0 },
              },
              {
                  $id: Now.ID['recent-incidents-list'],
                  component: 'list', // List component
                  componentProps: {
                      table: 'incident',
                      filter: 'active=true',
                      limit: 10,
                      columns: ['number', 'short_description', 'priority', 'state']
                  },
                  height: 8,
                  width: 6,
                  position: { x: 6, y: 0 },
              }
          ],
      },
      {
          $id: Now.ID['analytics'],
          name: 'Analytics',
          widgets: [
              {
                  $id: Now.ID['metrics-widget'],
                  component: 'single-score', // Single score component
                  componentProps: {
                      title: 'Key Metrics',
                      scoreSize: 'large'
                  },
                  height: 12,
                  width: 12,
                  position: { x: 0, y: 0 },
              }
]
```

### componentProps object

Configure the properties of widgets \[par\_dashboard\_widget\].

The available properties are determined by the component specified with the component property of the Dashboard object.

-   Trend data components require the dataSources, metrics, and trendBy properties. The groupBy property is optional.
-   Group data components require the dataSources, metrics, and groupBy properties. The trendBy property isn't supported in these visualizations.
-   Simple data components require the dataSources and metrics properties. The groupBy and trendBy properties aren't supported in these visualizations.

<table id="table_jgr_d1z_23c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

dataSources

</td><td>

Array

</td><td>

A list of data sources for the component. For example:```javascript
dataSources: [
  {
    label: "Incident", // Human-readable label
    sourceType: "table", // Type of data source
    tableOrViewName: "incident", // ServiceNow table name
    filterQuery: "", // Optional encoded query filter
    id: "data_source_1" // Unique data source ID
  },
...
]
```

</td></tr><tr><td>

headerTitle

</td><td>

String

</td><td>

A title to display with the widget.

</td></tr><tr><td>

metrics

</td><td>

Array

</td><td>

A list of metrics to measure for the data source. For example:```javascript
metrics: [
    {
        dataSource: 'data_source_1',  // Must match dataSource id
        id: 'metric_1',  // Unique metric ID
        aggregateFunction: 'AVG',  // COUNT, SUM, AVG, MIN, MAX, COUNT_DISTINCT
        aggregateField: 'business_duration'  // Field to be used for aggregation.
        axisId: 'primary',  // Which axis to display the series
    },
...
]
```

</td></tr><tr><td>

groupBy

</td><td>

Array

</td><td>

A list of configurations for grouping and organizing data by data source. For example:```javascript
groupBy: [
  {
    groupBy: [
      {
        dataSource: "data_source_1", // Must match dataSource id
        groupByField: "state" // Field to group by
      }
    ],
    maxNumberOfGroups: 10, // Maximum categories to show
    showOthers: false // Show "Others" category
  },
...
]
```

</td></tr><tr><td>

trendBy

</td><td>

Object

</td><td>

A configuration for trend charts. For example:```javascript
trendBy: {
  "trendByFrequency": "year", // Frequency of the trend (date, week, month, year)
  "trendByFields": [
    {
      "field": "sys_created_on", // Field to trend on (from the table of the dataSource)
      "metric": "metric_1" // ID of the metric
    }
  ]
}
```

</td></tr><tr><td>

sortBy

</td><td>

String

</td><td>

The method of sorting data.Valid values:

-   value
-   label
-   field

</td></tr></tbody>
</table>In the following example, the `line` component, which is a trend data type visualization, is used to show how a metric changes over time.

```javascript
{
    component: 'line',
    componentProps: {
        dataSources: [
            {
                label: 'Incident',
                sourceType: 'table',
                tableOrViewName: 'incident',
                filterQuery: '',
                id: 'data_source_1',
            },
        ],
        headerTitle: 'Incidents by State',
        metrics: [
            {
                dataSource: 'data_source_1',
                id: 'metric_1',
                aggregateFunction: 'COUNT',
                axisId: 'primary',
            },
        ],
        trendBy: {
            trendByFrequency: "year",
            trendByFields: [
                {
                    field: "sys_created_on",
                    metric: "metric_1"
                }
            ]
        },
    },
    height: 14,
    width: 17,
    position: { x: 0, y: 0 },
}
```

In the following example, the `single-score` component, which is a simple data type visualization, is used to show a single count metric.

```javascript
{
    component: 'single-score',
    componentProps: {
        dataSources: [
            {
                label: 'Incident',
                sourceType: 'table',
                tableOrViewName: 'incident',
                filterQuery: '',
                id: 'data_source_1',
            },
        ],
        headerTitle: 'Open Incidents',
        metrics: [
            {
                dataSource: 'data_source_1',
                id: 'metric_1',
                aggregateFunction: 'COUNT',
                axisId: 'primary',
            },
        ]
    },
    height: 14,
    width: 14,
    position: { x: 0, y: 0 },
}
```

## permissions array

Define permissions \[par\_dashboard\_permission\] to read, edit, and share a dashboard.

At least one of the user, group, or role properties must be specified for each permission in the array.

<table id="table_j3p_yqy_23c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

$id

</td><td>

String or Number

</td><td>

Required. A unique ID for the metadata object. When you build the application, this ID is hashed into a unique sys\_id. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).Format: `Now.ID['String' or Number]`

</td></tr><tr><td>

user

</td><td>

Reference or String

</td><td>

The variable identifier or sys\_id of a user \[sys\_user\] to which to grant permissions. To define a user, use the [Record API - ServiceNow Fluent](record-api-now-ts.md#).

</td></tr><tr><td>

group

</td><td>

Reference or String

</td><td>

The variable identifier or sys\_id of a user group \[sys\_user\_group\] to which to grant permissions. To define a user, use the [Record API - ServiceNow Fluent](record-api-now-ts.md#).

</td></tr><tr><td>

role

</td><td>

Reference or String

</td><td>

The variable identifier or sys\_id of a role \[sys\_user\_role\] to which to grant permissions. To define a user, use the [Role API - ServiceNow Fluent](role-api-now-ts.md#).

</td></tr><tr><td>

canRead

</td><td>

Boolean

</td><td>

Flag that indicates whether the user, group, or role can view the dashboard.Default: true

</td></tr><tr><td>

canWrite

</td><td>

Boolean

</td><td>

Flag that indicates whether the user, group, or role can edit the dashboard.Default: false

</td></tr><tr><td>

canShare

</td><td>

Boolean

</td><td>

Flag that indicates whether the user, group, or role can share the dashboard.Default: false

</td></tr><tr><td>

owner

</td><td>

Boolean

</td><td>

Flag that indicates whether the user, group, or role is the owner of the dashboard. For at least one user, the owner property should be set to true.Default: false

</td></tr></tbody>
</table>```javascript
permissions: [
        {
            $id: Now.ID['manager-user-permission'],
            user: 'a8f98bb0eb32010045e1a5115206fe3a', // sys_id of manager user
            canRead: true,
            canWrite: true,
            owner: true,
        },
        {
            $id: Now.ID['itil-role-permission'],
            role: '2831a114c611228501d4ea6c309d626d', // sys_id of itil role
            canRead: true,
            canWrite: false,
        },
        {
            $id: Now.ID['support-group-permission'],
            group: 'd625dccec0a8016700a222a0f7900d06', // sys_id of Service Desk group
            canRead: true,
            canWrite: false,
        }
]
```

## visibilities array

Define visibility rules \[par\_dashboard\_visibility\] for which UX experiences display the dashboard.

<table id="table_j3p_yqy_23c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

$id

</td><td>

String or Number

</td><td>

Required. A unique ID for the metadata object. When you build the application, this ID is hashed into a unique sys\_id. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).Format: `Now.ID['String' or Number]`

</td></tr><tr><td>

experience

</td><td>

Reference or String

</td><td>

Required. The variable identifier of a Workspace object or sys\_id of a UX application \[sys\_ux\_page\_registry\]. For more information, see [Workspace API - ServiceNow Fluent](fluent-workspace-api.md#).

</td></tr></tbody>
</table>```javascript
visibilities: [
  {
    $id: Now.ID["dashboard_visibility_1"],
    experience: myWorkspace // Reference to Workspace object
  }
]
```

