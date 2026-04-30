---
title: Configure the formula builder
description: Specify the formula context, the tables, and the identifiers before you can build a formula.
locale: en-US
release: zurich
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Formula building in a calculated metric definition, Configure, GRC: Metrics in Integrated Risk Management, Risk Management, Governance, Risk, and Compliance]
---

# Configure the formula builder

Specify the formula context, the tables, and the identifiers before you can build a formula.

## Before you begin

Role required: admin

## About this task

It’s necessary to configure the formula builder before a formula can be built in a calculated metric definition. During configuring, you can specify the formula context, the tables to use, and their conditions.

## Procedure

1.  Navigate to **All** &gt; **Formula builder** &gt; **Configuration**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_lkw_gq1_kzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Formula context

</td><td>

Configuration available to create the formula for a specific option. The choices for Risk are as follows:-   **Calculation level - entity \(Risk\)**
-   **Calculation level - metric definition \(Risk\)**
**Note:** Users of other applications can select different context options.

</td></tr><tr><td>

Application

</td><td>

Scope of the application. This field is automatically set.

</td></tr><tr><td>

Table

</td><td>

Tables that you want to use while building the formula.

</td></tr><tr><td>

Condition

</td><td>

Criteria using which the records are filtered from the selected table when building the formula. For example, you can build a condition that **Domain is Risk**.

</td></tr><tr><td>

Display field

</td><td>

Unique display name for the operands such as the **Name** field or the **ID** field.

</td></tr><tr><td>

Identifier

</td><td>

An abbreviated two-letter combination of lowercase letters that is associated with a specific table name. For example, if your table name is Hardware accessories, your identifier can be `ha`.**Note:** Using `fn` as an identifier isn’t permitted as fn refers to function.

</td></tr><tr><td>

Show additional columns

</td><td>

Option to decide if you want additional columns to be displayed.**Note:** This option is useful in cases where there are duplicate emission factor names. Showing additional details can help metric managers to select the right emission factor.

</td></tr><tr><td>

Primary column

</td><td>

Primary column that you 'd like displayed.**Note:** This field appears only when the **Show additional columns** option is selected.

</td></tr><tr><td>

Secondary column

</td><td>

Secondary column that you'd like displayed.**Note:** This field appears only when the **Show additional columns** option is selected.

</td></tr><tr><td>

Primary column label

</td><td>

Preferred label of the primary column selected.**Note:** This field appears only when the **Show additional columns** option is selected.

</td></tr><tr><td>

Secondary column label

</td><td>

Preferred label of the secondary column selected.**Note:** This field appears only when the **Show additional columns** option is selected.

</td></tr></tbody>
</table>4.  Select **Submit**.


**Parent Topic:**[Formula building in a calculated metric definition](../concept/formula-building-at-metric-definition-and-entity-level-irm.md)

