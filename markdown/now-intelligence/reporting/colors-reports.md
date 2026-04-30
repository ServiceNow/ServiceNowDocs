---
title: Predefined colors in reports
description: Depending on the type and configuration of the report, you can select one color, a predefined color palette, or predefined chart colors. All three options are built on a customizable set of individual colors.
locale: en-US
release: zurich
product: Reporting
classification: reporting
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Advanced Core UI reporting topics, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Predefined colors in reports

Depending on the type and configuration of the report, you can select one color, a predefined color palette, or predefined chart colors. All three options are built on a customizable set of individual colors.

If you aren’t grouping or stacking the data in a report, you select one color. If you stack or group data, you have two main choices for colors:

-   **Color palette**

    A sequence of colors applied to the elements in a chart. The colors repeat in order from highest value to lowest. Use color palettes in reports when you want the colors of the reports to denote order. Reports using the same palette use the same colors regardless of what data they’re showing.

    In the following example, you see two reports on incidents that are grouped by different fields, Priority and Category. Both reports use the default color palette, and both show the same colors.

    ![Two reports using the same color palette and therefore the same colors.](../image/reports-with-color-palette.png)

-   **Chart colors**

    Chart colors always apply the same color to the same grouping or stacking value. Different grouping and stacking values in different reports have different colors. Use chart colors if, for example, you always want an element like Priority &gt; 1 - Critical to have the same color.

    In the following example, you see two reports on incidents that are grouped by the same field, Priority. Both reports use the chart colors. The same values of Priority have the same color despite being in a different order.

    ![Two reports grouped by the same field and using chart colors.](../image/reports-chart-colors-priority.png)

    In the following example, the reports are grouped by different fields and use the chart colors. The bars are in different colors, as each element has a unique color.

    ![Two reports using chart colors but grouped by different fields, thus using different colors.](../image/report-chart-colors-diff-fields.png)


Both the color palettes and the chart colors use the colors defined in the Color Definition \[sys\_report\_color\] table. A report admin can add more colors.

**Note:** If neither a color palette nor the chart colors are suitable for your report, you can enter a set of hexadecimal color codes. These codes are independent of the defined colors.

-   **[Color palettes](color-palettes.md)**  
A color palette is a sequence of colors that apply to the elements in a chart, in order from highest value to lowest. All reports that use the same palette use the same colors.
-   **[Chart colors](c_ChartColors.md#)**  
Chart colors assign a consistent color to a grouping or stacking value in reports. The color stays the same across reports regardless of the order of the values.
-   **[Define system colors for analytics](../task/t_DefiningSystemColors.md)**  
Create color definitions for use in reports and Performance Analytics widgets.

**Parent Topic:**[Advanced Core UI reporting topics](c_AdvancedReporting.md)

