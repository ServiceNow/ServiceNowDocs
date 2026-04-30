---
title: Define system colors for analytics
description: Create color definitions for use in reports and Performance Analytics widgets.
locale: en-US
release: xanadu
product: Reporting
classification: reporting
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Predefined colors in reports, Advanced reporting topics, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Define system colors for analytics

Create color definitions for use in reports and Performance Analytics widgets.

## Before you begin

Role required: report\_admin.

## About this task

The following visualizations use the colors that you define in the Color Definitions \[sys\_report\_color\] table:

-   Reports with one color
-   Reports with a color palette
-   Reports using chart colors
-   Performance Analytics breakdown widgets
-   Performance Analytics time series widgets with widget indicators
-   Data Visualization Next Experience Components that use a single color, a color palette, or fixed element colors \(chart colors\)
-   Performance Analytics target color schemes

For reports and visualizations with a color palette and for Performance Analytics widgets, these colors are used via chart color schemes. Chart colors reference color definitions directly.

## Procedure

1.  Navigate to **All** &gt; **Reports** &gt; **Administration** &gt; **Color Definition**.

2.  Click **New**.

3.  Fill in these fields.

<table id="table_sk1_1n1_kp"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a unique name for the new color.

</td></tr><tr><td>

Color

</td><td>

Enter a hexadecimal value, for example \#003366.

</td></tr><tr><td>

Themeable color

</td><td>

Applies an alternate color from the UX Theme Properties \[sys\_ux\_theme\_property\] table to use when a theme is applied. Colors in the UX Theme Properties table may have different values depending on which theme variant in the UX Themes \[sys\_ux\_theme\] table is applied to your instance. To learn more about theming, see [Themes in Next Experience](https://www.servicenow.com/docs/access?context=next-experience-theming&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

 When a theme is turned on, the system applies this color to classic reports and visualizations created by the data visualization component. If no themeable color is defined, the system uses the color defined in the **Color** field.

 When themes are turned off, the system applies this color to visualizations created by the data visualization component only. The system applies the color defined in the **Color** field to classic reports and ignores the **Themeable color** field.

</td></tr></tbody>
</table>4.  Click **Submit**.


**Parent Topic:**[Predefined colors in reports](../concept/colors-reports.md)

