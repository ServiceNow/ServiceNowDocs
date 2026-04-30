---
title: Create a metric template
description: Create a metric template to define reusable rating scales for evaluating non-scripted metrics.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Assessment administrator tasks, Using assessments, Assessments, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a metric template

Create a metric template to define reusable rating scales for evaluating non-scripted metrics.

## Before you begin

Role required: assessment\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Assessments** &gt; **Metric Definition** &gt; **Templates**.

2.  Click **New**.

3.  Fill in the **Name** field on the Assessment Metric Template form.

4.  To use images for template choices, such as for image scale questions, select **Allow Image**.

5.  Click **Submit**.

6.  Under the **Assessment Template Definitions** related list, click **New**.

    Create a template definition for each answer option you want to appear on an assessment question.

7.  Fill in the following fields:

    -   **Display:** Enter the text to appear as the answer option.
    -   **Value:** Enter a numeric value, equal to or greater than zero, that you want the answer option to equate to. Values are used in results calculations.
    -   **Selected Image**: Click to add the image to use for selected state.
    -   **Unselected Image**: Click to add the image to use for unselected state.
    When you view assessment questions that use templates, answer options appear in order from least to greatest Value.

    **Tip:** To prevent reporting confusion, no two template definitions for a given template should have the same Value.

8.  Click **Update**.


-   **[Metric templates](../reference/r_MetricTemplates.md)**  
Metric templates define reusable rating scales for evaluating non-scripted metrics.
-   **[Update a metric minimum and maximum value to match a template](t_UpdAMetrMinMaxValToMatchATmplate.md)**  
For assessment results to be properly calculated, the Min and Max values of a metric that uses a template must be equal to the smallest and largest template definition Value, respectively.

**Parent Topic:**[Assessment administrator tasks](../concept/c_AssessmentProcess.md)

**Related topics**  


[Assessment metrics](../concept/c_AssessmentMetrics.md)

[Create an assessment metric for a category](t_CreateAMetric.md)

[Create an assessment metric definition](t_CreateAMetricDefinition.md)

