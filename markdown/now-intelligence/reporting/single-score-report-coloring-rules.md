---
title: Create coloring rules for single score reports
description: Configure rules for how numerical values are displayed in single score reports, to highlight why a value is important.
locale: en-US
release: australia
product: Reporting
classification: reporting
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Administering reports, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Create coloring rules for single score reports

Configure rules for how numerical values are displayed in single score reports, to highlight why a value is important.

## Before you begin

Role required: itil, report\_user, report\_group, report\_global, report\_admin, or admin.

This task is part of configuring the style options of a single score report.

See [Single score data visualization example](../../par-for-workspace/task/dv-example-single-score.md) for example steps to implement a coloring rule.

## Procedure

1.  On the **Style** tab of the Report Designer, click **Edit coloring rules**.

2.  In the **Multilevel Pivot Rules \[Single Score Color Rule view\]** dialog box, select **New rule**.

3.  Fill in the fields on the form.

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

The font color to apply to values that match this rule. Select the search icon \(![](../image/SearchIcon.png)\) to choose colors from an existing list or enter a hexadecimal color value.

</td></tr><tr><td>

Rule order \(Optional\)

</td><td>

A numerical value that determines the order in which the color rules apply. Rules are evaluated from lowest value to highest. For example, one rule applies the color blue to the value 7 and a second rule applies the color red to values from 1 through 10. If you want the 7 to appear blue, the **Rule order** value for the first rule should be higher so that the second rule doesn’t override it.

 If you don’t specify a rule order, the coloring rules are applied in the order in which they were created.

</td></tr></tbody>
</table>4.  Click **Submit** to save the rule and create a new rule, or click **OK** to save the rule and return to the Report Designer.


## Result

The colors you specify in the rules apply to the single score report that you’re editing.

**Parent Topic:**[Administering reports](../concept/c_AdminsteringReports.md)

