---
title: Color schemes
description: When a data visualization illustrates multiple indicators, breakdowns, or table fields, the colors of the different values can follow a color scheme.Create a reusable set of colors available for reports, Performance Analytics widgets, and Platform Analytics data visualization components.
locale: en-US
release: yokohama
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Performance Analytics widgets, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Color schemes

When a data visualization illustrates multiple indicators, breakdowns, or table fields, the colors of the different values can follow a color scheme.

Color schemes can apply to the following visualizations:

-   Time series and breakdown widgets that display multiple indicators or breakdowns
-   Widgets on breakdown dashboards when multiple elements are shown separately
-   Reports that group by or stack by table fields
-   Platform Analytics data visualization components that group by or stack by table fields

You can select a color scheme in the **Color Scheme** field when you create a widget. For an example, see [Create a pie, donut, or semi-donut visualization for a breakdown widget](../task/create-pie-widget.md). You can also design your own color scheme.

You don’t have to specify a color scheme. In this case, the default color scheme specified in the property **com.snc.pa.chart\_default\_color\_schema** is applied if necessary. In the base system, this color scheme is Default UI14.

All color schemes are on the Chart color scheme \[pa\_chart\_color\_schemes\] table, at **Performance Analytics** &gt; **System** &gt; **Chart Color Schemes**.

The default color schemes use color definitions with the Qualitative themeable colors from the UX Theme Properties \[sys\_ux\_theme\_property\] table. When Next Experience is activated, these colors are used rather than the Core UI color palette.

**Related topics**  


[Predefined colors in reports](../../reporting/concept/colors-reports.md)

[Report types](../../reporting/reference/report-types-creation-details-rd.md)

## Create a color scheme

Create a reusable set of colors available for reports, Performance Analytics widgets, and Platform Analytics data visualization components.

### Before you begin

Role required: pa\_power\_user or pa\_admin

### About this task

**Tip:** A ServiceNow AI Platform or Reporting admin can create custom colors for use in your color schemes. For more information, see [Define system colors for analytics](../../reporting/task/t_DefiningSystemColors.md).

### Procedure

1.  Navigate to **All** &gt; **Platform Analytics Administration** &gt; **Color Settings** &gt; **Chart Color Schemes**.

2.  Click **New**.

3.  Enter a descriptive **Name**.

4.  Select colors in the **Color 1** and **Color 2** fields.

    A color scheme must have at least two colors. You can use more.

5.  Select up to 32 total colors to include in the color scheme.

6.  Click **Submit**.


