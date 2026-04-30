---
title: Reporting properties
description: Use properties to fine-tune report behavior and appearance.
locale: en-US
release: yokohama
product: Reporting
classification: reporting
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [Reporting reference, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Reporting properties

Use properties to fine-tune report behavior and appearance.

## Introduction

Navigate to **Reports** &gt; **Administration** &gt; **Properties** to configure the main reporting properties. In the Filter navigator, enter `sys_properties.list` to configure other reporting properties.

## Reporting properties

<table id="table_c14_tv3_5r"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable Natural Language Queries \(NLQ\) in Report Designer

 com.snc.par.nlq.report\_designer.enabled

</td><td>

-   Type: true \| false
-   Default value: true
-   Location: **Reports** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

Truncates x-axis labels to 20 characters. \(Applicable only to charts generated with the charting v2 plugin\)

glide.chart.truncate.x\_axis\_labels

</td><td>

-   Type: true \| false
-   Default value: true
-   Location: **Reports** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

glide.ui.chart.bar.horiz.max\_col\_slant\_labels

</td><td>

Sets the maximum number of columns in a horizontal bar chart before slanting \(angling\) the labels.-   Type: integer
-   Default value: 5
-   Location: [Add the property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US) to the System Property \[sys\_properties\] table.

</td></tr><tr><td>

Toggle animations on and off for charts generated with the charting v2 plugin

glide.chart.animation

</td><td>

Enables animations for reports and Performance Analytics visualizations that support animations. **Note:** Map reports do not support animations and therefore do not follow this property.

 -   Type: true \| false
-   Default value: true
-   Location: **Reports** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

Sets the default truncation for truncated values.

glide.chart.data\_labels.remove\_leading

</td><td>

When enabled, the default truncation is left side. When disabled, the default is right side truncation. -   Type: string
-   Default value: false
-   Location: **Reports** &gt; **Administration** &gt; **Properties**

 This property is applicable only if glide.chart.truncate.data\_labels is set.

</td></tr><tr><td>

Number of bins in a histogram chart \(minimum 1, maximum 20\)

glide.chart.histogram.bins

</td><td>

Determines the number of sections that appear on the Y axis of the histogram.-   Type: integer
-   Default value: 10 \(Allowed range of values 1–20\)
-   Location: **Reports** &gt; **Administration** &gt; **Properties**

 This property applies to histogram reports.

</td></tr><tr><td>

Color of the mean value dot in box and trendbox charts.

glide.chart.box.mean.color

</td><td>

Sets the color of the 'mean' value dot in a box or trendbox report. -   Type: string
-   Default value: \#2f7ed8
-   Location: **Reports** &gt; **Administration** &gt; **Properties**

 This property applies to box and trendbox reports.

</td></tr><tr><td>

glide.chart.drill.open\_new\_win

</td><td>

If enabled, opens the default list drilldown in a new tab if no drilldown is defined. Applies only for non-list type reports.-   Type: true \| false
-   Default value: false
-   Location: **Reports** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

Color of the box and whisker in box charts

glide.chart.box.color

</td><td>

Sets the color of the box report. -   Type: string
-   Default value: \#FF0000
-   Location: **Reports** &gt; **Administration** &gt; **Properties**

 This property applies to box reports.

</td></tr><tr><td>

Default Color list name for each dataset

glide.ui.report.datasets.default\_colors

</td><td>

Sets the default colors to use when adding multiple data sets to a single chart. These values are used when the **Chart color** value is **Use one color**. Enter a comma-separated list of chart color **Color name** values. You can view available colors and define new colors on the Chart Colors \[sys\_report\_chart\_color\] table.

 Each color is used in order as the default chart color when adding a data set to a chart. If there are more data sets than default colors, the colors repeat.

 -   Type: string
-   Default value: Default Color
-   Location: **Reports** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

List of color palette names that are used as a default color palette for each dataset

glide.ui.report.datasets.default\_palettes

</td><td>

Sets the default palette to use when adding multiple data sets to a single chart. These values are used when the **Chart color** value is **Use color palette**. Enter a comma-separated list of chart color scheme **Name** values. You can view the available palettes and define new palettes on the Chart Color Schemes \[pa\_chart\_color\_schemes\] table.

 Each palette is used in order as the default chart palette when adding a data set to a chart. If there are more data sets than default palettes, the palettes repeat.

 -   Type: string
-   Default value: Default UI14
-   Location: **Reports** &gt; **Administration** &gt; **Properties**

 This property applies to pie, bar, horizontal bar, donut, and semi-donut reports.

</td></tr><tr><td>

Set the default map for reports of type 'Map'

glide.ui.report.map.default\_map

</td><td>

Specifies the default map to use when creating Map-type reports.-   Type: string
-   Default value: world
-   Location: **Reports** &gt; **Administration** &gt; **Properties**

 This property applies to Map reports.

</td></tr><tr><td>

glide.ui.chart.color

</td><td>

Specify the chart color. -   Type: string
-   Default value: \#006DDA
-   Location: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US) to the System Property \[sys\_properties\] table.

</td></tr><tr><td>

glide.ui.chart.use\_full\_color\_palette

</td><td>

Enable this property to generate bars in bar and Pareto charts with different colors for each bar.-   Type: true \| false
-   Default value: \#false
-   Location: **Reports** &gt; **Administration** &gt; **Properties**

 This property applies to bar, horizontal bar, and Pareto reports.

</td></tr><tr><td>

glide.chart.label.legend.truncate\_to

</td><td>

Truncates legend labels for left or right legend alignment for all chart sizes except large charts. Prevents shrinking of charts when labels are too long.-   Type: integer
-   Default value: 14
-   Location: System Property `[sys_properties]` table

</td></tr><tr><td>

glide.chart.label.legend.truncate\_to.large

</td><td>

Truncates legend labels for left or right legend alignment for large charts. Prevents shrinking of charts when labels are too long.-   Type: integer
-   Default value: 20
-   Location: System Property `[sys_properties]` table

</td></tr><tr><td>

glide.report.new\_calendar

</td><td>

-   Type: true \| false
-   Default value: true
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

glide.report.calendar.max\_days\_back

</td><td>

Enables you to specify the number of days with events that are returned when you browse backward and forward in a calendar report. Evaluated on the **Calendar by** field in the report creator. -   Type: integer
-   Default value: 30
-   Location: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US) to the System Property \[sys\_properties\] table.

 This property applies to calendar reports.

</td></tr><tr><td>

glide.report.calendar.default\_event\_duration

</td><td>

The default duration for an event without a specified end date.-   Type: string
-   Default value: 01:00:00 \(One hour, zero minutes, zero seconds\)
-   Location: System Property `[sys_properties]` table

 This property applies to calendar reports.

</td></tr><tr><td>

glide.report.calendar.max\_more\_events\_per\_day

</td><td>

Defines the maximum number of calendar events that can appear in the **+ &lt;number&gt;** pop-up window for:-   A calendar day when calendar is in month or year view
-   The top 'full day' section of a calendar day when a calendar is in day or week view

 When this number is exceeded, a **+ many** link appears, which opens a list of events instead of a pop-up. For more information, see system property **glide.report.calendar.max\_events\_displayed\_per\_cell**.

 -   Type: integer
-   Default value: 30
-   Location: [Add the property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US) to the System Property \[sys\_properties\] table.

</td></tr><tr><td>

glide.report.calendar.max\_events\_displayed\_per\_cell

</td><td>

Defines the maximum number of events that can appear in calendar report for: -   A calendar day when calendar is in month or year view
-   The top 'full day' section of a calendar day when a calendar is in day or week view

 Events that exceed this value are visible via a link in the calendar cell. See **glide.report.calendar.max\_more\_events\_per\_day** for more information.

 -   Type: integer
-   Default value: 3
-   Location: [Add the property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US) to the System Property \[sys\_properties\] table.

</td></tr><tr><td>

glide.ui.report.extend\_calendar\_choices

</td><td>

Controls which field styles are applied during calendar highlighting. If this property is set to false, field styles in only the Task table are used. If this property is set to true, the calendar first uses field styles from the table that the report is based on. If no applicable styles exist in that table, the calendar uses field styles from the Task table.-   Type: true \| false
-   Default value: true
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

glide.ui.filter.first\_day\_of\_week

</td><td>

Identifies the first day of the calendar week for the company. By default, the start of the week is Monday, meaning that the calendar week begins with Monday and ends with Sunday. To change this behavior, add the property **glide.ui.filter.first\_day\_of\_week** to the instance as an integer property. Enter the integer corresponding with the day of the week that the calendar begins on. 1 is Sunday, 2 is Monday, and so on. The function impacts all charts and calculations where the day of the week is used as a parameter.-   Type: integer
-   Default value: 2
-   Location: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US) to the System Property \[sys\_properties\] table.

</td></tr><tr><td>

glide.ui.chart.bar.horiz.max\_col\_slant\_labels

</td><td>

Sets the maximum number of columns in a horizontal bar chart before slanting \(angling\) the labels.-   Type: integer
-   Default value: 5
-   Location: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US) to the System Property \[sys\_properties\] table.

 This property applies to horizontal bar reports.

</td></tr><tr><td>

glide.ui.chart.pie.labels

</td><td>

Enables \(true\) or disables \(false\) labels on pie chart slices.-   Type: true \| false
-   Default value: true
-   Location: [Add the property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US) to the System Property \[sys\_properties\] table.

</td></tr><tr><td>

glide.ui.chart.pie.labels.max\_items

</td><td>

Sets the maximum number of pie chart slice values that can be returned to display their labels.-   Type: integer
-   Default value: 8
-   Location: [Add the property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US) to the System Property \[sys\_properties\] table.

</td></tr><tr><td>

glide.chart.data.label.truncate\_to

</td><td>

Sets the maximum length of a data label for a chart. If longer, the label is truncated and an ellipsis \(…\) appended. **Note:** This property does not apply to stacked bar chart reports.

 -   Type: integer
-   Default value: 13
-   Location: System Property `[sys_properties]` table

</td></tr><tr><td>

glide.report.pivot.fixed\_headers

</td><td>

When disabled, the header row of a multiple level pivot table is unfrozen and scrolls out of frame when the user scrolls through the table.

 -   Type: true \| false
-   Default value: true
-   Location: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US) to the System Property \[sys\_properties\] table.

 This property applies to multilevel pivot tables.

</td></tr><tr><td>

glide.report.metric\_max\_data\_points

</td><td>

Configure the maximum number of data points per MetricBase report. Typically only MetricBase time series reports display enough data to require this limitation.-   Type: integer
-   Default value: 2000
-   Location: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US) to the System Property \[sys\_properties\] table.

</td></tr><tr><td>

glide.report.metric\_max\_series

</td><td>

Configure the number of series per data set in a MetricBase report.-   Type: integer
-   Default value: 20
-   Maximum value: 100
-   Location: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US) to the System Property \[sys\_properties\] table.

</td></tr><tr><td>

glide.report.report\_view.read\_acl

</td><td>

Configure READ-level security on report execution. -   Type: string
-   Default value: enforce
-   Possible values:
    -   **ignore**

No evaluation is conducted against the read ACL and all users can see the report as if they had passed the ACL.

    -   **enforce**

Evaluation is conducted against the read ACL. Users can only view the report if they pass the read ACL.

    -   **log**

The read ACL check is not enforced, but the administrator can see which users would have been blocked if the security check was enforced.

-   Location: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US) to the System Property \[sys\_properties\] table.

</td></tr></tbody>
</table>## Interactive Filters properties

<table id="table_vpt_zpy_w1b"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.homepage\_interactivity.ui\_ctrls\_max\_display\_options

</td><td>

Maximum number of choices for radio button and check box interactive filters.-   Type: integer
-   Default value: 25
-   Location: **Reports** &gt; **Administration** &gt; **Properties**

 Category: Choice list, Reference field, Date, Group

</td></tr></tbody>
</table>**Parent Topic:**[Reporting reference](../concept/reporting-reference.md)

