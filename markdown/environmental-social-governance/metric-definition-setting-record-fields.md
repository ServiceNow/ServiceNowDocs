---
title: Metric definition setting record fields
description: The fields of the metric definition setting record form are explained in this topic.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/environmental-social-governance/metric-definition-setting-record-fields.html
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure a metric definition setting record, Formula building in a calculated metric definition, Configuring GRC: Metrics, GRC: Metrics, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Metric definition setting record fields

The fields of the metric definition setting record form are explained in this topic.

<table id="table_bd2_qpr_bhc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the record. For example, `Default record for CMD calculations`.

</td></tr><tr><td>

Active

</td><td>

Option to mark the default values record as active.

</td></tr><tr><td>

One for null record

</td><td>

You can select relevant operators in the field. The system assigns a default value of 1 to null or undefined operands when the adjacent operator matches your selection. This ensures the calculation proceeds without error.

</td></tr><tr><td>

Order

</td><td>

Determines the priority of the record when multiple records are available. The record which has the highest number is selected

</td></tr><tr><td>

Skip null record

</td><td>

You can select relevant operators in the field. If a metric operand is null or undefined during formula execution and the adjacent operator matches the one selected, the system will skip that operand from the calculation. This prevents errors and ensures the formula continues without interruption.

</td></tr><tr><td>

Zero for null record

</td><td>

You can select relevant operators in the field. If a metric operand is null or undefined during formula execution, the system checks the adjacent operator. When the operator matches one selected in this field, the system assigns a value of 0 to that operand. This ensures the calculation proceeds without error and maintains consistency in results. This field is available only when Type is All or Calculated metric definition.

</td></tr><tr><td>

Type

</td><td>

Determines which fields display on the form and which table the setting applies to. The available options are:

-   All: Applies to every metric, metric definition, and calculated metric definition. Table name and Filter are hidden.
-   Metric definition: Applies to automated and manual metric definitions. Table name is set to Metric Definition.
-   Calculated metric definition: Applies to calculated metric definitions. Table name is set to Calculated Metric Definition.
-   Metric: Applies to individual metrics. Table name is set to Metric.

</td></tr><tr><td>

Table name

</td><td>

Displays the table the setting applies to, based on the selected Type. **Note:** This field is hidden when Type is All.

</td></tr><tr><td>

Filter

</td><td>

Specifies the condition under which the setting applies to records on the table shown in Table name. You can set up multiple criteria conditions.**Note:** This field is hidden when Type is All.

</td></tr><tr><td>

Variance base value

</td><td>

Value the system uses to calculate variance when the previous period value is null or zero. This field is available for all Type selections. When more than one active record applies to a metric, the system uses the most specific Type first. The order is Metric, then Metric definition or Calculated metric definition, then All. The system uses Order to break ties within the same Type.

</td></tr></tbody>
</table>**Parent Topic:**[Configure a metric definition setting record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/activate-default-values-for-cmd-calculations.md)

