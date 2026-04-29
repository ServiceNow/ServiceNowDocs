---
title: Create a context variable for the target source type PA Indicator
description: Create a context variable manually for the target source type PA Indicator if the breakdown is of Choice list type.
locale: en-US
release: australia
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring target source for target automation, Configuring goals in Strategic Planning, Configure, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Create a context variable for the target source type PA Indicator

Create a context variable manually for the target source type PA Indicator if the breakdown is of Choice list type.

## Before you begin

Select the Goal Framework for SPM scope for the application.

Role required: sn\_gf.goal\_admin

## About this task

The context variable provides information that can be used to fetch the required data and auto-update the Actual value on the Target form. After a context variable is created for the target source, the goal user can configure the Actual Value Source Configuration section on the Target form for the Actual value to get auto-updated.

Creating a context variable is similar to creating a column on a table.

## Procedure

1.  Navigate to **All** &gt; **Enterprise Goal Management** &gt; **Target Sources**.

2.  Open the required target source that you want to create a context variable for.

3.  In the Context Variables related list, click **New**.

4.  On the form, fill in the **Type** field as Choice and the other fields as needed.

    For a description of the field values, see [Context Variable form](../reference/context-variable-form-apw.md).

5.  Click **Submit**.

    A context variable of choice type is created.

6.  In the Choices related list of the context variable you created, click **New**.

    **Note:** If you don’t see the Choices related list on the Context Variable form, add it by navigating to **Configure** &gt; **Related Lists** on the form.

7.  On the form, fill in the fields.

<table id="table_demand_benefit_plan_form"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Name of the context variable for which the choice is created.

</td></tr><tr><td>

Element

</td><td>

Column name in the context variable form for which the choice is created.

</td></tr><tr><td>

Label

</td><td>

Name of the choice.

</td></tr><tr><td>

Value

</td><td>

Sys\_id of the choice value for which the context variable is created. You can copy the sys\_id from the Choices related list of the Dictionary Entry \[sys\_dictionary\] table.

</td></tr></tbody>
</table>8.  Click **Submit**.

9.  Repeat the steps 6 through 8 to create more choices for the context variable.


## What to do next

The goal user can configure these choices as context variables on the Target form for which the target source is configured.

**Parent Topic:**[Configuring target source for target automation](../concept/setting-targets-for-a-goal-and-automating-the-actual-value-using-agf-apw.md)

