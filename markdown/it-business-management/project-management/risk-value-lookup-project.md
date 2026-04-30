---
title: Configure custom Risk rank and Risk value for a project
description: Configure custom risk rank and value scores \(such as High-Medium, Medium-Low, or Absolute-Low\) to rate the impact and probability factors for a risk.
locale: en-US
release: xanadu
product: Project Management
classification: project-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Add risks for a project, RIDAC records for a project in Project Workspace, Define a project, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Configure custom Risk rank and Risk value for a project

Configure custom risk rank and value scores \(such as High-Medium, Medium-Low, or Absolute-Low\) to rate the impact and probability factors for a risk.

## Before you begin

Role required: pps\_admin

## About this task

Use the Risk Value Lookup module to set up the risk rank and risk value for a specific combination of risk impact and probability. The system uses these values to determine the degree of risk \(Absolute, High, Medium, Low\) based on the impact and probability factors of a risk.

The value in the **Probability** field is multiplied by the value of the **Impact** field to generate the values for the **Risk rank** and corresponding **Risk value** in the Risk form.

By default, you can use the following impact, value, and probability scores for a risk to create a risk rank and risk value score:

-   Absolute
-   Low
-   Medium or Moderate
-   High

For example, a risk might have high probability and medium impact but you might want to consider it as an overall low risk for the project. In that case, you would configure the Risk Value Matcher form with the following values:

-   Impact = 2 Medium
-   Risk Rank Color = Green
-   Probability = High
-   Probability Number = 1
-   Risk Value = 3 Low

The following image illustrates the results of this example on the Risk form.![Risk rank and risk value in the Risk form](../image/risk-value-matcher.png)

## Procedure

1.  Navigate to **All** &gt; **Project Administration** &gt; **Settings** &gt; **Risk Value Lookup**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_d34_qsl_zjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Impact

</td><td>

Impact value of the risk.The default values are:

-   1 = High
-   2 = Medium
-   3 = Low


</td></tr><tr><td>

Application

</td><td>

The application to which these risk values belong.

</td></tr><tr><td>

Risk Rank Color

</td><td>

Color to indicate the severity of the risk. **Tip:** You can enter variations of a color to differentiate between risks with similar impact and probability values. For example, you could enter **lightgreen** to indicate a low-severity risk.

</td></tr><tr><td>

Risk Value

</td><td>

The value for the specified risk impact and probability combination.The options are: High, Medium, and Low.

 This value is displayed in the **Risk value** field of the Risk form.

</td></tr><tr><td>

Probability

</td><td>

Risk probability value to associate with the impact value of the risk. The options are: Absolute, High, Moderate, and Low.

</td></tr><tr><td>

Probability Number

</td><td>

Numerical value to indicate the probability. This value is multiplied by the value of the **Impact** field for calculating risk rank.The default values are:

-   1 = Absolute
-   1 = High
-   2 = Moderate
-   3 = Low
 The calculated risk rank and the risk rank color are displayed in the **Risk rank** field of the Risk form.

</td></tr></tbody>
</table>4.  Click **Submit**.


**Parent Topic:**[Add risks for a project](add-risks-for-project.md)

