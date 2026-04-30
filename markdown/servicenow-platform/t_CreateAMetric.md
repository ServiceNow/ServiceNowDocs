---
title: Create an assessment metric for a category
description: After you create a category, create metrics you can use to evaluate the assessable records for that category.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Assessment metrics, Assessment administrator tasks, Using assessments, Assessments, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create an assessment metric for a category

After you create a category, create metrics you can use to evaluate the assessable records for that category.

## Before you begin

Role required: assessment\_admin or admin

## About this task

When you create metrics, consider the focus of the category and what characteristics you want to measure for the items you will assess.

## Procedure

1.  Navigate in one of the following ways.

<table id="choicetable_amk_2gr_z4"><tbody><tr><td id="d536482e69">

**__Assessments__ &gt; __Metric Definition__ &gt; __Categories__**

</td><td>

Open a category, and locate the **Assessment Metrics** related list.

 This is the suggested navigation path, as the system links metrics to the category from which they are created.

</td></tr><tr><td id="d536482e99">

**__Assessments__ &gt; __Metric Definition__ &gt; __Metrics__**

</td><td>

 

</td></tr></tbody>
</table>2.  Click **New**.

3.  On the Assessment Metric form, fill in the fields.

    For a description of the field values, see [Assessment Metric form for a category](../reference/assessment-metric-category-form.md).

4.  Save the record.

    When you create a **Choice** or **Likert Scale** question, reopen the Assessment Metric form after you submit it to create a metric definition. If you distribute a questionnaire without creating the answers for questions with these data types, recipients are unable to answer the quesitons. If the questions are mandatory, the recipients are unable to submit their questionnaires.


-   **[Create an assessment metric definition](t_CreateAMetricDefinition.md)**  
Metrics with Choice or Likert Scale data types must have metric definitions defined to represent answer options on questionnaires.
-   **[Change the order of an answer](t_ChangeTheOrderOfAnAnswer.md)**  
By default, the order of answer options is established when a question is created with a data type of **Choice** or **Likert Scale**.
-   **[Metric types and assessable records](../concept/c_MetricTypesAndAssessableRecords.md)**  
In the Assessments application, assessment administrators create and administer metric types and assessable records.

**Parent Topic:**[Assessment metrics](../concept/c_AssessmentMetrics.md)

**Related topics**  


[Assessment metrics](../concept/c_AssessmentMetrics.md)

[Create an assessment metric definition](t_CreateAMetricDefinition.md)

[Update a metric minimum and maximum value to match a template](t_UpdAMetrMinMaxValToMatchATmplate.md)

