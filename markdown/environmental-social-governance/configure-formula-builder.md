---
title: Configure the formula builder
description: Specify the formula context, the tables, and the identifiers before you can build a formula.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Formula building in a calculated metric definition, Configuring GRC: Metrics, GRC: Metrics, Environmental, Social, and Governance Management]
---

# Configure the formula builder

Specify the formula context, the tables, and the identifiers before you can build a formula.

## Before you begin

Role required: admin

## About this task

It’s necessary to configure the formula builder before a formula can be built in a calculated metric definition. During configuring, you can specify the formula context, the tables to use, and their conditions. In the context of ESG Management, if you build the formula at the metric definition level, you must select the metric definition table and the metric table during configuration. To build the formula at the entity level, you must select the metric definition and the emission factor table. Other applications can use the tables that are required for their use. You can configure the columns and their labels that you want to display along with the emission factor during building the formula. These labels help in easily identifying the emission factors.

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

Configuration available to create the formula for a specific option. The choices for ESG are as follows:-   **Calculation level - entity**
-   **Calculation level - metric definition**
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

Criteria using which the records are filtered from the selected table when building the formula. For example, you can build a condition that **Domain is ESG**.

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

Primary column that you 'd like displayed for the emission factor during formula building. For example, if you select **From unit**, then the emission factor's From unit will be displayed along with the factor name.

</td></tr><tr><td>

Secondary column

</td><td>

Secondary column that you'd like displayed for the emission factor during formula building. For example, if you select **To unit**, then the emission factor's To unit will be displayed along with the factor name.**Note:** When defining calculated metric definitions, you can use emission factors with different units than the collected data.

</td></tr><tr><td>

Primary column label

</td><td>

Preferred label of the primary column selected. For example, if you selected **Short Description** in the **Primary column** field, you can provide the preferred label as `Short Desc`.

</td></tr><tr><td>

Secondary column label

</td><td>

Preferred label of the secondary column selected.

</td></tr></tbody>
</table>4.  Select **Submit**.


**Parent Topic:**[Formula building in a calculated metric definition](../concept/formula-building-at-metric-definition-and-entity-level.md)

