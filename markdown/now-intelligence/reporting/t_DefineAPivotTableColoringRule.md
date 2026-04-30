---
title: Create coloring rules for multilevel pivot reports
description: Configure rules for how numerical values are displayed in a multilevel pivot table report. Coloring rules make it easy to highlight the more important values. The color rule is applied to the content of cells in pivot reports.
locale: en-US
release: zurich
product: Reporting
classification: reporting
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Administering reports, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Create coloring rules for multilevel pivot reports

Configure rules for how numerical values are displayed in a multilevel pivot table report. Coloring rules make it easy to highlight the more important values. The color rule is applied to the content of cells in pivot reports.

## Before you begin

Role required: report\_admin or admin

**Note:** It isn’t possible to apply coloring rules to the Total cells in multilevel pivot reports.

## Procedure

1.  On the **Style** tab of the Report Designer, select **Edit coloring rules**.

    If you see the error message 'Security constraints prevent access to requested page,' an access control list is preventing access. If necessary, one with the security\_admin role should create read and write access control lists \(ACLs\) on the Multilevel Pivot Rule \[sys\_report\_mpivot\_rule\] table.

2.  In the Multilevel Pivot Rules dialog box, select **New rule**.

3.  Fill in the fields on the form.

<table id="table_pyf_5xj_2s"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Operator

</td><td>

The operator used when evaluating values in cells, such as **greater than** or **between**. For example, to style cells with a value less than 5, select **lower than** and specify a **Value 1** value of 5.

</td></tr><tr><td>

Value 1

</td><td>

The number to evaluate cell values against. When the **Operator** value is **between**, enter the lower value in the **Value 1** field.**Note:** When creating rules based on a duration value, specify the duration in seconds.

</td></tr><tr><td>

Value 2

</td><td>

The maximum value that a cell can contain to match this rule. This field only appears when the **Operator** value is **between**.

</td></tr><tr><td>

Font color

</td><td>

The font color to apply to cells that match this rule.

</td></tr><tr><td>

Background color

</td><td>

The background color to apply to cells that match this rule. This option applies only to multilevel pivot table reports.

</td></tr><tr><td>

Rule order

</td><td>

A numerical value that determines the order in which the rules apply. Rules with a higher rule order apply later and override lower-order rules. For example, one rule matches cells with a value greater than 140, and another rule matches cells with a value lower than 150. The rule with the higher order applies to cells with values from 141 through 149.

</td></tr></tbody>
</table>4.  Select **Submit** to save the rule and create another rule, or select **OK** to save the rule and return to the Report Designer.


**Parent Topic:**[Administering reports](../concept/c_AdminsteringReports.md)

