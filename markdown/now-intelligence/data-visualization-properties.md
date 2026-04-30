---
title: Data Visualization properties
description: Several properties that limit what can be displayed in data visualizations.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Data Visualization properties

Several properties that limit what can be displayed in data visualizations.

These Platform Analytics data visualization properties are available in the System Properties \[sys\_properties\] table.

**Note:** To open the System Properties table, enter `sys_properties.list.do` in the navigation filter.

<table id="table_zjb_bhr_3dc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

com.glide.par.pae.drilldown\_to\_core\_ui

</td><td>

Applies only to Platform Analytics experience:

 When true, **Go to data** chart interactions for visualizations of tables open the Core UI list of table records. Redirections in general that open lists or visualizations open Core UI lists and visualizations.

 When false, **Go to data** chart interactions for visualizations of tables open the Platform Analytics list of table records. Redirections in general that open lists or charts open Platform Analytics lists and charts.

 For more information, see [Chart interactions in a data visualization](../concept/dv-chart-interactions.md).

 -   Type: true \| false \(Boolean\)
-   Default value: true
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

par\_vis\_config.data\_source.can\_select\_indicator

</td><td>

Specifies roles \(comma-separated\) which can select indicators as data sources from the Data Visualization configuration panel. If empty, all users can select the indicator sources that they have access to.-   Type: string
-   Default value: empty
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

par\_vis\_config.live\_refresh\_rate\_min\_value

</td><td>

Specifies the minimum interval in seconds for the Live refresh rate setting in the Data Visualization configuration. If set, a user can still set an empty or 0 value.-   Type: integer
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

</td></tr></tbody>
</table>**Parent Topic:**[Data visualization reference](data-visualization-reference.md)

