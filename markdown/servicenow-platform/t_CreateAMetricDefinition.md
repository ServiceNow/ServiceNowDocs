---
title: Create an assessment metric definition
description: Metrics with Choice or Likert Scale data types must have metric definitions defined to represent answer options on questionnaires.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create an assessment metric for a category, Assessment metrics, Assessment administrator tasks, Using assessments, Assessments, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create an assessment metric definition

Metrics with Choice or Likert Scale data types must have metric definitions defined to represent answer options on questionnaires.

## Before you begin

Role required: assessment\_admin or admin

## About this task

Each metric definition appears as one answer option for a question on an assessment questionnaire. For example, a metric for the question "How satisfied are you with the quality of this vendor?" has three metric definitions to create these answer options: **Very satisfied**, **Somewhat satisfied**, and **Not at all satisfied**.

## Procedure

1.  Open the metric record you want to edit.

2.  In the **Assessment Metric Definitions** related list, click **New** to create a new metric definition.

3.  Fill in the fields:

    -   **Display:** Enter the text you want to appear as the answer option.
    -   **Value:** Enter the numeric value, greater than or equal to zero, to which the answer option equates. Values are used to calculate metric results. When you view assessment questions, metric definitions appear in order from least to greatest value.
        -   The system sets the minimum and maximum values according to the metric definition values.
        -   To prevent reporting confusion, no two metric definitions for a given metric should have the same Value.
4.  Click **Submit**.


**Parent Topic:**[Create an assessment metric for a category](t_CreateAMetric.md)

**Related topics**  


[Assessment metrics](../concept/c_AssessmentMetrics.md)

[Metric templates](../reference/r_MetricTemplates.md)

