---
title: Color palettes
description: A color palette is a sequence of colors that apply to the elements in a chart, in order from highest value to lowest. All reports that use the same palette use the same colors.
locale: en-US
release: xanadu
product: Reporting
classification: reporting
topic_type: concept
last_updated: "2024-10-22"
reading_time_minutes: 1
breadcrumb: [Predefined colors in reports, Advanced reporting topics, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Color palettes

A color palette is a sequence of colors that apply to the elements in a chart, in order from highest value to lowest. All reports that use the same palette use the same colors.

The following reports can use a color palette. Select a color palette on the **Style** tab of the Report Designer:

-   Pie charts
-   Bar and column charts that have a **Stack by** or **Group by** value
-   Line and trend reports that have a **Stack by** or **Group by** value

Color palettes are defined in the Chart color scheme \[pa\_chart\_color\_schemes\] table. Report admins have read access to this table. Navigate to **All** &gt; **Platform Analytics Administration** &gt; **Color Settings** &gt; **Chart Color Schemes**.

**Tip:** A ServiceNow AI Platform or Performance Analytics admin can create custom Core UI color palettes. For more information, see [Create a color scheme](../../performance-analytics/concept/color-schemes-pa-widgets.md#).

The default color schemes use color definitions with the Qualitative themeable colors from the UX Theme Properties \[sys\_ux\_theme\_property\] table. When Next Experience is activated, these colors are used rather than the Core UI color palette.

## Color palette

In the following example, you see two reports on incidents that are grouped by different fields, Priority and Category. Both reports use the default color palette, and both show the same colors.

![Two reports using the same color palette and therefore the same colors.](../image/reports-with-color-palette.png)

**Parent Topic:**[Predefined colors in reports](colors-reports.md)

