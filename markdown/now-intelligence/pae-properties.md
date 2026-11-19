---
title: Platform Analytics experience properties
description: Several properties affect data visualizations and the ability to create Core UI artifacts in the Platform Analytics experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/now-intelligence/pae-properties.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [report, responsive dashboards, data visualizations]
breadcrumb: [Reference, Platform Analytics experience, Platform Analytics]
---

# Platform Analytics experience properties

Several properties affect data visualizations and the ability to create Core UI artifacts in the Platform Analytics experience.

## Data visualization properties

These Platform Analytics data visualization properties are available in the System Properties \[sys\_properties\] table.

**Note:** To open the System Properties table, enter `sys_properties.list.do` in the navigation filter.

<table id="table_dv-properties-pae"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

com.glide.par.pae.drilldown\_to\_core\_ui

</td><td>

Applies only to Platform Analytics experience:

 When true, **Go to data** chart interactions for visualizations of tables open the Core UI list of table records. Redirections in general that open lists or visualizations open Core UI lists and visualizations.

 When false, **Go to data** chart interactions for visualizations of tables open the Platform Analytics list of table records. Redirections in general that open lists or charts open Platform Analytics lists and charts.

 For more information, see [Chart interactions in a data visualization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/dv-chart-interactions.md).

 -   Type: true \| false \(Boolean\)
-   Default value: true
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

par\_vis\_config.data\_source.can\_select\_indicator

</td><td>

Specifies roles \(comma-separated\) which can select indicators as data sources from the data visualization configuration panel. If empty, all users can select the indicator sources that they have access to.-   Type: string
-   Default value: empty
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

par\_vis\_config.live\_refresh\_rate\_min\_value

</td><td>

Specifies the minimum interval in seconds for the Live refresh rate setting in the data visualization configuration. If set, a user can still set an empty or 0 value.-   Type: integer
-   Default value: 30 \(seconds\)
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

par\_viz.table\_data.max\_data\_points

</td><td>

Maximum number of data points for data visualizations based on table sources.-   Type: integer
-   Default value: 10000
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

par\_viz.table\_data.max\_groups

</td><td>

Maximum setting recognized for the maxNumberOfGroups property of data visualizations that have a Group by. Applies only to table data.-   Type: integer
-   Default value: 50
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_analytics\_list.pagination\_max\_value

</td><td>

Maximum number of records per page in a List visualization in Platform Analytics experience.**Danger**

Raising this property above 100 might lead to memory issues.

-   Type: integer
-   Default value: 100
-   Location: System Property \[sys\_properties\] table

</td></tr></tbody>
</table>## Core UI artifact properties

The following properties affect the ability to create Core UI dashboards and reports from within the Dashboard and Data visualization libraries, respectively. They exist in the Properties \[sys\_properties\] table.

**Important:**

-   The properties exist by default only on upgraded instances.
-   The properties have no effect on instances that were net new on Xanadu or a later release. You cannot create Core UI artifacts on such instances.

<table id="table_sfl_k3y_qkc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

com.snc.par.coreui.dashboard\_create.enabled

</td><td>

Enables any user with an internal role to create a Core UI dashboard by selecting **Create new** in the Dashboards library. If absent or false, only a user with the dashboard\_admin role or higher can create a Core UI dashboard, and only in the Dashboards \[pa-dashboard\] table.-   Type: true \| false \(Boolean\)
-   Default value: true
-   Location: System Property \[sys\_properties\] table. Exists only on upgraded instances.

</td></tr><tr><td>

com.snc.par.coreui.report\_create.enabled

</td><td>

Enables any user with an internal role to create a Core UI report by selecting **Create new** in the Data visualizations library. If absent or false, only a user with the report\_admin role or higher can create a Core UI report, and only in the Reports \[sys\_report\] table.-   Type: true \| false \(Boolean\)
-   Default value: true
-   Location: System Property \[sys\_properties\] table. Exists only on upgraded instances.

</td></tr></tbody>
</table>**Parent Topic:**[Platform Analytics experience reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/platform-analytics-exp-reference.md)

