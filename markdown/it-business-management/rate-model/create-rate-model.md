---
title: Create or modify a rate model
description: Create or modify a rate model that can be linked to a project or demand to determine planned costs and actuals for their resource. The rate model provides date-effective, criteria-driven hourly rates for these investments.
locale: en-US
release: zurich
product: Rate Model
classification: rate-model
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Rate Models, Project Portfolio Management, Strategic Portfolio Management]
---

# Create or modify a rate model

Create or modify a rate model that can be linked to a project or demand to determine planned costs and actuals for their resource. The rate model provides date-effective, criteria-driven hourly rates for these investments.

## Before you begin

-   Choose the attributes to define the criteria in a rate model to derive hourly rates.
-   Define the [budget reference rates](../../project-management/concept/c_BudgetReferenceRates.md) for the non-functional currency for the required time periods.
-   Role required: pps\_admin or it\_rate\_model\_admin

## Procedure

1.  Create a rate model.

<table id="create-rate-model-option"><thead><tr><th align="left" id="d170233e71">

Option

</th><th align="left" id="d170233e74">

Steps

</th></tr></thead><tbody><tr><td id="d170233e80">

**From Project Administration**

</td><td>

1.  Navigate to **All** &gt; **Project Administration** &gt; **Rate Model** &gt; **All**.
2.  Click **New**.


</td></tr><tr><td id="d170233e116">

**From Time Sheets**

</td><td>

1.  Navigate to **All** &gt; **Time Sheets** &gt; **Rate Model** &gt; **All**.
2.  Click **New**.


</td></tr></tbody>
</table>2.  On the form, fill in the fields.

<table id="table_cwy_r3n_cfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the rate model.

</td></tr><tr><td>

Active

</td><td>

Option for indicating the status of the rate model. Only active rate models can be assigned to a project or demand.

</td></tr><tr><td>

Default

</td><td>

Option for setting the rate model as the default. You can set only one rate model as default.

 A default rate model is automatically associated to new projects and demands.

</td></tr><tr><td>

Rate model context

</td><td>

Context set for the rate model.Read-only system field.

</td></tr><tr><td>

Currency

</td><td>

Default currency for the rate lines in the rate model.

</td></tr><tr><td>

Rate type

</td><td>

Option for enabling the rate type attribute on rate lines in the rate model.When selected, **Rate type** is added as one of the attributes along with other defined attributes. For more information, see [Rate type in labor rate card](../../cost-management/concept/RateType.md).

</td></tr><tr><td>

Description

</td><td>

Short description for the rate model.

</td></tr></tbody>
</table>3.  Click **Submit**.


## What to do next

[Add attributes from a set of predefined entities](define-rate-model-criteria.md) to define the criteria for rate model to derive resource cost.

**Parent Topic:**[Rate Models](../concept/rate-model.md)

