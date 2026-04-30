---
title: Create a unit family
description: Create a unit family to group similar units together. For example, the various units of distance such as miles and kilometers can be grouped. Unit families help you to organize units during unit conversion.
locale: en-US
release: xanadu
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring metrics, GRC: Metrics in Integrated Risk Management, Risk Management, Governance, Risk, and Compliance]
---

# Create a unit family

Create a unit family to group similar units together. For example, the various units of distance such as miles and kilometers can be grouped. Unit families help you to organize units during unit conversion.

## Before you begin

Role required: admin

## About this task

Creating unit families also supports conversion of units. Sometimes, the unit in which metric data is entered may be different from the reporting unit of the metric definition. In such cases, the units must be converted. For example, the metric data may be entered in US gallons and the reporting unit in the metric definition is Liters. If US gallon and liters belong to the same unit family such as Volume, you can convert the units.

Various formulas are used to convert different units. If the reporting unit of a metric definition belongs to a unit family that has the conversion factor as **Calculated**, then the metric data tasks for that metric must be provided in the same unit as the metric definition. For example, if the reporting unit for temperature in a metric definition is Celsius, and if the conversion factor of temperature is set to **Calculated**, then all the metric data tasks for that metric definition can only be provided in Celsius. In such cases, users can specify the formula that must be used for the conversion. For more information see, [Formula building in a calculated metric definition](../concept/formula-building-at-metric-definition-and-entity-level.md).

## Procedure

1.  Navigate to **All** &gt; **Risk** &gt; **Administration** &gt; **Unit family**

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_cd2_ll2_25b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the unit family. For example, `Temperature`.

</td></tr><tr><td>

Conversion factor

</td><td>

Conversion factor that must be applied when converting units from the family. The choices are as follows:-   **Direct**: Use this option if the conversion of the units in the family can be done directly. For example, you can convert kilometers to miles using direct conversion.
-   **Calculated**: Use this option if the conversion formulas are complex. For example, to convert temperatures in degrees Celsius to Fahrenheit, the formula is °F = °C × \(9/5\) + 32.


</td></tr></tbody>
</table>4.  Select **Submit**.


