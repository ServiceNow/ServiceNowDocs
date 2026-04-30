---
title: Colors in data visualizations
description: Depending on the data visualization, you can select different colors: a fixed color for each Group by element, a predefined color palette, a spectrum spanning high and low values, or a single color.Configure rules for how numerical values are displayed, to easily highlight why a value is important.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Platform Analytics]
---

# Colors in data visualizations

Depending on the data visualization, you can select different colors: a fixed color for each Group by element, a predefined color palette, a spectrum spanning high and low values, or a single color.

By default, the data visualization uses the colors that are set in the UX Theme \[sys\_ux\_theme\] used by the instance. These colors in turn are defined in the UX theme properties \[sys\_ux\_theme\_properties\] table. Themes include the following colors:

-   A default single color
-   A default color palette
-   A default spectrum of shades for a color range

In a specific visualization, you can override the colors set in the UX theme. Set colors in the Colors subsection of the Presentation section in the visualization's configuration panel. The available options are described in the "Create a..." topic for each visualization type.

## Selecting a single value color or a color per metric

You can select a single value color for any visualizations except gauge and pie/donut. When you select a single color, you are at first offered the default color. You can choose a color instead in the **Set value color** field. Interacting with that field opens a selector where you can choose a color by color icon or from a list. The list also shows you an icon for each entry. The selector also has a search field. Entering a value into that search field shows you a list of colors filtered by the search term, which can be plain language or part of a hexadecimal code.

If the data visualization shows more than one metric, you can select a single color for each metric.

![Color selector when selecting by icon](../../par-for-workspace/image/select-color-by-icon-dv.png "Color selector in icon and list modes") ![Color selector when selecting by list](../../par-for-workspace/image/select-color-by-list-dv.png "Color selector in icon and list modes") ![Color selector using search term.](../../par-for-workspace/image/select-color-search-dv.png "Color selector in icon and list modes")

## Color rules for pivot table, dial, and single score visualizations

Single score, dial, and pivot table visualizations can use a single color that is set dynamically when the data meets certain conditions. For example, you can create a rule to show the score in green for values under 25. For more information, see [Create coloring rules for data visualizations](colors-dv.md#).

## Color options for Group by values from table data sources

If you group by a value in a visualization based on a Table data source, you have the following two color range options:

-   **Color palette**

    A sequence of colors applied to the Group by elements. The colors repeat in order from highest value to lowest. Use color palettes in data visualizations when you want the colors to denote order. Visualizations that use the same palette use the same colors regardless of what data they’re showing.

    Color palettes are the default coloring pattern in a data visualization where a Group by value is defined. If you don’t specify a color palette, the color palette from the UX theme is used.

    Non-default color palettes are defined in the Chart color scheme \[pa\_chart\_color\_schemes\] table. The admin or pa\_admin role is required to create a color palette. For more information, see [Create a color scheme](color-schemes-pa-widgets.md#).

    In the following example, you see two data visualizations that show incidents. One visualization shows incidents grouped by Priority, and the other visualization shows incidents grouped by Category. Both visualizations use the Blues dark to light \(6\) color palette, which uses six shades of blue. Both visualizations show the same colors for the same ranking of values, although the values are different.

    ![The same color palette applied to two different Group by values](../../par-for-workspace/image/dv-color-palette.png)

-   **Fixed element colors**

    Fixed element colors always apply the same color to the same grouping or stacking value. Different grouping and stacking values in different visualizations have different colors. Use fixed element colors if, for example, you always want an element like Priority &gt; 1 - Critical to have the same color.

    **Important:**

    Fixed element colors are only available for visualizations of Table data sources.

    When an element appears for the first time in a data visualization that is using fixed element colors, a color is defined for that element. Thereafter that element has the same color in any data visualization that shows it. The colors are stored for each element in the Chart Colors \[sys\_report\_chart\_color\] table. To change the color assigned to an element, you need the admin or report\_admin role. For more information, see [Define colors for data categories](../../reporting/concept/c_ChartColors.md#).

    In the following example, you see two data visualizations that show incidents that are grouped by the same field, Priority. Both visualizations use fixed element colors. The same values of Priority have the same color despite being in a different order.

    ![Two data visualizations grouped by the same field and using fixed element colors.](../../par-for-workspace/image/dv-fixed-element-color.png)

    In the following example, the data visualizations are grouped by different fields and use fixed element colors. The bars are in different colors, because each element has a unique color.

    ![Two data visualizations using fixed element colors but grouped by different elements, thus using different colors.](../../par-for-workspace/image/dv-fixed-color-scheme.png)


**Parent Topic:**[Platform Analytics](c_performanceAnalyticsAndReporting.md)

**Related topics**  


[Working with themes in Next Experience](https://www.servicenow.com/docs/access?context=next-experience-theming&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)

## Create coloring rules for data visualizations

Configure rules for how numerical values are displayed, to easily highlight why a value is important.

### Before you begin

Role required: Any role, and editing rights to the visualization

This task is part of configuring the display settings of some data visualizations.

### Procedure

1.  Open the data visualization for editing, either in the dashboard in-line editor or the Visualization Designer.

    For more information, see [Edit a data visualization in an inline dashboard](../../dashboards/task/editing-dv-in-line-db.md) or [Edit a data visualization in the Visualization Designer](../../dashboards/task/edit-dv-ac-center.md).

2.  In the **Presentation** area of the configuration panel, open the **Colors** section.

3.  Choose the **Single Color** type and select **Add rule**.

    ![The Color Rules section under Colors, under Presentation, in the Configuration panel of a data visualization.](../../reporting/image/dv-color-rule-in-panel.png)

4.  Fill in the fields on the form.

<table id="table_pyf_5xj_2s"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Operator

</td><td>

The operator used when evaluating values, such as **greater than** or **between**. For example, to style values of less than 5, select **lower than** and specify a **Value 1** value of 5.

</td></tr><tr><td>

Value 1

</td><td>

The number to evaluate cell values against. When the **Operator** value is **between**, enter the lower value in the **Value 1** field.**Note:**

-   The color rule is applied to the aggregated values.
-   When creating rules based on a duration value, specify the duration in seconds.


</td></tr><tr><td>

Value 2

</td><td>

The maximum value to match this rule. This field only appears when the **Operator** value is **between**.

</td></tr><tr><td>

Font color

</td><td>

The font color to apply to values that match this rule.

</td></tr><tr><td>

Rule order \(Optional\)

</td><td>

A numerical value that determines the order in which rules apply. Rules are evaluated from lowest value to highest. For example, you have one rule applies the color blue to the value 7, and a second rule that applies the color red to values between 1 and 10. If you want the 7 to appear blue, the **Rule order** value for the first rule should be higher so that the second rule does not override it.

 If you do not specify a rule order, coloring rules are applied in the order in which they were created.

</td></tr></tbody>
</table>5.  Select **Apply** to save the rule.

    Create a new rule or return to the Visualization Designer.


