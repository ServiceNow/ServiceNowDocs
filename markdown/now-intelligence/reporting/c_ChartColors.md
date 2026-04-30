---
title: Chart colors
description: Chart colors assign a consistent color to a grouping or stacking value in reports. The color stays the same across reports regardless of the order of the values.You can define a chart color for a data category in reports, such as critical priority incidents. You can select a predefined color or specify a hexadecimal code.
locale: en-US
release: yokohama
product: Reporting
classification: reporting
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Predefined colors in reports, Advanced reporting topics, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Chart colors

Chart colors assign a consistent color to a grouping or stacking value in reports. The color stays the same across reports regardless of the order of the values.

**Note:** This topic refers to Reporting in the Core UI. If your instance is migrated to Platform Analytics experience, see [Colors in data visualizations](../../performance-analytics/concept/colors-dv.md#).

## Using chart colors in a report

Chart colors, if defined, are available in the **Chart colors** menu in the Style tab of the Report Designer.

## How chart colors work

When a data category appears for the first time in a report that uses chart colors, a record is added automatically to the Chart Colors \[sys\_report\_chart\_color\] table. The following fields define the data category on the Chart Colors record:

-   Data source
-   Stacking or grouping element
-   Element value
-   Application scope

The Chart Colors record also specifies a color. When a Chart Colors record is created automatically, the color is assigned from the UI 14 Color Definition \[sys\_report\_color\] records. You can edit the chart color to use a different color definition or a hexadecimal color code. For more information about editing chart colors, see the section "Define colors for data categories".

**Note:**

-   The base system includes several predefined chart colors. Platform Analytics Solutions can provide more chart colors.
-   The UI 14 color definitions use the Datavis - Qualitative themeable colors from the UX Theme Properties \[sys\_ux\_theme\_property\] table. Next Experience must be activated for these colors to be used. Otherwise, the fallback colors from the color definitions are used.

Any other report that uses chart colors and that shows the same data category references the same Chart Colors record. Because the reports reference the same record, they show the same data category in the same color. For example, you create the first report that uses chart colors and shows priority 1 incidents in the Global scope. A Chart Colors record is created automatically to associate such incidents with a color. All other reports that use chart colors and show priority 1 incidents in the Global scope show them in the same color.

## Chart colors

In the following example, you see two reports on incidents that are grouped by the same field, Priority. Both reports use the chart colors, as set in the Style tab of the Report Designer. The same values of Priority have the same color despite being in a different order.

![Two reports grouped by the same field and using chart colors.](../image/reports-chart-colors-priority.png)

**Parent Topic:**[Predefined colors in reports](colors-reports.md)

## Define colors for data categories

You can define a chart color for a data category in reports, such as critical priority incidents. You can select a predefined color or specify a hexadecimal code.

### Before you begin

Role required: report\_admin.

### Procedure

1.  Navigate to **All** &gt; **Reports** &gt; **Administration** &gt; **Chart Colors**.

2.  Click **New**.

    ![New chart colors form](../image/new-chart-colors-form.png "New Chart Colors form")

3.  Fill in the fields, as appropriate.

<table id="table_sk1_1n1_kp"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Table used for the report.**Note:** The list shows only tables and database views that are [in the same scope](https://www.servicenow.com/docs/access?context=c_ApplicationScope&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US) as the chart colors record.

</td></tr><tr id="row_h2z_tfw_1z"><td>

Element

</td><td>

Column name specific to the selected table.

</td></tr><tr id="row_tqq_5fw_1z"><td>

Value

</td><td>

The value of the element for which the specified color applies. The value is case-sensitive.For elements that are reference type fields, Value is the sys\_id of the value for which the specified color applies.

 The following example shows how the values of the state element on Choice \[sys\_choice\] records match the values of the state element on Chart Color \[sys\_report\_chart\_color\] records.

 ![Chart color choice type example - part 2](../image/chart-color-choice-type-ex-pt2.png)

 ![Chart color choice type example - part 1](../image/chart-color-choice-type-ex-pt1.png)

 To understand the various ways to get a record's sys\_id, see [The unique record identifier \(sys\_id\)](https://www.servicenow.com/docs/access?context=c_UniqueRecordIdentifier&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

</td></tr><tr id="row_xqw_5fw_1z"><td>

Color name

</td><td>

Color selected from the Color Definitions \[sys\_report\_color\] table. If you select a color definition, it overrides the color specified in the **Color** field. For more information about color definitions, see [Define system colors for analytics](../task/t_DefiningSystemColors.md).

</td></tr><tr id="row_p3b_vfw_1z"><td>

Color

</td><td>

Hexadecimal value used to specify a color that is not defined in the Color Definition table.

**Note:** If the **Color name** field contains a value, the **Color** field is ignored.

</td></tr></tbody>
</table>4.  Click **Submit**.


### Result

The value selected in the **Element** field for the table in the **Name** field is displayed with the specified color.

The chart color is now available for reports on the table, in the Style tab of the Report Designer.

