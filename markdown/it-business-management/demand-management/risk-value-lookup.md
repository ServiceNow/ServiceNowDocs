---
title: Configure custom Risk rank and Risk value for a demand
description: Configure custom risk rank and value scores \(such as High-Medium, Medium-Low, or Absolute-Low\) to rate the impact and probability factors for a risk.
locale: en-US
release: xanadu
product: Demand Management
classification: demand-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Add risks for a demand, RIDAC \(Risk, Issue, Decision, Action, and Request Changes\) records, Use, Demand Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Configure custom Risk rank and Risk value for a demand

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

For example, a risk might have high probability and medium impact but you might want to consider it as an overall low risk for the demand. In that case, you would configure the Risk Value Matcher form with the following values:

-   Impact = 2 Medium
-   Risk Rank Color = Green
-   Probability = High
-   Probability Number = 1
-   Risk Value = 3 Low

The following image illustrates the results of this example on the Risk form.![Risk rank and risk value in the Risk form](../../project-management/image/risk-value-matcher.png)

## Procedure

1.  Navigate to **All** &gt; **Project Administration** &gt; **Settings** &gt; **Risk Value Lookup**.

2.  Click **New**.

3.  On the risk value matcher form, fill in the fields.

    For a description of the field names, see [Risk value matcher form](../reference/risk-value-matcher-form.md).

4.  Click **Submit**.


**Parent Topic:**[Add risks for a demand](add-risks-for-demand.md)

