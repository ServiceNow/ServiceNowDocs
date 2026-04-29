---
title: Create a rate line
description: In a rate model, create a rate line to define an hourly rate based on a set of criteria for a given date range.
locale: en-US
release: australia
product: Rate Model
classification: rate-model
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Rate Models, Project Portfolio Management, Strategic Portfolio Management]
---

# Create a rate line

In a rate model, create a rate line to define an hourly rate based on a set of criteria for a given date range.

## Before you begin

-   [Define criteria and add rate model attributes](define-rate-model-criteria.md)
-   Role required: pps\_admin or it\_rate\_model\_admin

## About this task

Before creating or updating a rate line, note the following points:

-   Rate lines with the same set of criteria values cannot have overlapping dates.
-   A criteria field can be empty.
-   All criteria fields on the form have a value `All other (*)` that, if selected, is considered by the rate model if no exact match exists for that criteria.
-   To use a non-functional \(non-default\) currency in a rate line, ensure that the corresponding [budget reference rate](../../project-management/concept/c_BudgetReferenceRates.md) is available.

## Procedure

1.  Open a rate model by performing one of the following actions:

    -   Navigate to **All** &gt; **Project Administration** &gt; **Rate Model** &gt; **All**.
    -   Navigate to **All** &gt; **Time Sheets** &gt; **Rate Model** &gt; **All**.
2.  On the Rate Model form, click the **View Rate Lines** related link.

3.  On the Rate Lines form, click **New**.

4.  On the form, fill in the fields.

<table id="table_n22_fxd_gfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Rate Model

</td><td>

Rate model the rate line belongs to.

</td></tr><tr><td>

Start date

</td><td>

Start date of the time period in which the rate is applicable.

</td></tr><tr><td>

End date

</td><td>

End date of the time period in which the rate is applicable.

</td></tr><tr><td>

Criteria fields

</td><td>

Fields corresponding to the rate model attributes added to define the criteria. The number of fields may vary.For example, if you have added Group and Location as rate model attributes, they are available as fields on the form where you can specify their values.

</td></tr><tr><td>

Rate

</td><td>

Applicable rate and currency of the rate line. By default, the currency of the rate model to which the rate line belongs is selected as the currency. You can select a rate currency, which can be different from the rate model currency. Rate lines with the same set of criteria values and currency must not have overlapping dates.

 A project or demand manager can track the resource cost for projects or demands in the corresponding project or demand currency by installing the PPM Standard Multicurrency \(com.snc.ppm\_multicurrency\) plugin and enabling the Project Currency view or Demand Currency view for resource plans. For more information, see the [Create a resource plan](../../resource-management/task/t_CreateResourcePlanProjectTask.md) topic.

</td></tr><tr><td>

Rate Type

</td><td>

Labor rate type applicable for the rate line.The field appears if the **Rate type** check box on the Rate Model form is selected.

</td></tr><tr><td>

Rate in functional currency

</td><td>

Rate in the default currency configured in the Financial Management application. This field is not editable.

</td></tr></tbody>
</table>5.  Click **Submit**.


## Result

Rate lines that represent resource hourly rates based on defined attributes are created.

**Parent Topic:**[Rate Models](../concept/rate-model.md)

