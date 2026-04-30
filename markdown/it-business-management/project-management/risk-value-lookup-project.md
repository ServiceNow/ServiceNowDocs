---
title: Configure custom Risk rank and Risk value for a project
description: Configure custom risk rank and value scores \(such as High-Medium, Medium-Low, or Absolute-Low\) to rate the impact and probability factors for a risk.
locale: en-US
release: yokohama
product: Project Management
classification: project-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Add risks for a project, Adding RIDAC \(Risks, Issues, Actions, Decisions, and Request Changes\) records for a project, Use, Project Management, Project Portfolio Management, Strategic Portfolio Management]
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

## Procedure

1.  Navigate to **All** &gt; **Project Administration** &gt; **Settings** &gt; **Risk Value Lookup**.

2.  Select **New**.

3.  On the form, fill in the fields.

    For more information, see [Risk value matcher form](../../planning-and-policy/reference/risk-value-matcher-form.md).

4.  Select **Submit**.


**Related topics**  


[Adding RIDAC \(Risks, Issues, Actions, Decisions, and Request Changes\) records for a project](../concept/ridac-entries-for-project.md)

[Convert one RIDAC \(Risk, Issue, Decision, Action, and Request Changes\) record to another for a project](convert-ridac-for-project.md)

[Associate existing RIDAC \(Risks, Issues, Actions, Decisions, and Request Changes\) records for a project](reassociate-ridac-project.md)

