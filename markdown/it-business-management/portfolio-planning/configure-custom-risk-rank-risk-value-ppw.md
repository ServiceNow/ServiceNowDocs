---
title: Configure a custom risk rank and risk value
description: Configure custom risk ranks and value scores to rate the impact and probability factors for a risk.
locale: en-US
release: australia
product: Portfolio Planning
classification: portfolio-planning
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Next Experience for Demand Management in Portfolio Planning, Portfolio Planning, Strategic Portfolio Management]
---

# Configure a custom risk rank and risk value

Configure custom risk ranks and value scores to rate the impact and probability factors for a risk.

## Before you begin

Role required: pps\_admin

## About this task

Use the Risk Value Lookup module to set up the risk rank and risk value for a specific combination of risk impact and probability. The system uses these values to determine the degree of risk \(Absolute, High, Medium, and Low\) based on the impact and probability factors of a risk.

The value in the **Probability** field is multiplied by the value of the **Impact** field to generate the values for the **Risk rank** and corresponding **Risk value** in the Create New Risk form.

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

In this case, the calculated risk rank and value are as follows:

-   Calculated risk rank = 2
-   Calculated risk value = 2

The following image illustrates a Risk form.![Risk rank and risk value in the Risk form](../../planning-and-policy/image/risk-value-form-color.png)

## Procedure

1.  Navigate to **All** &gt; **Project Administration** &gt; **Settings** &gt; **Risk Value Lookup**.

2.  Select **New**.

3.  On the risk value lookup form, fill in the fields.

    For a description of the field names, see [Risk value lookup form](../reference/risk-value-lookup-form-ppw.md).

4.  Select **Submit**.


