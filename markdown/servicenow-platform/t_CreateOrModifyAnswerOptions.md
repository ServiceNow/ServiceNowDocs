---
title: Create or modify answer options
description: You must create answer options, called metric definitions, for survey questions that have Data type set to Choice or Likert Scale.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Survey questions, Survey administration, Using surveys, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create or modify answer options

You must create answer options, called metric definitions, for survey questions that have **Data type** set to **Choice** or **Likert Scale**.

## Before you begin

Role required: admin or survey\_admin

## About this task

Changes to a survey, such as the addition or modification of answer options, apply to existing survey instances immediately.

## Procedure

1.  Navigate to **All** &gt; **Survey** &gt; **Questions**.

2.  Open a choice or Likert scale survey question.

3.  In the **Assessment Metric Definitions** related list, open a metric definition or click **New**.

    Each answer option is stored as a record on the Assessment Metric Definition \[asmt\_metric\_definition\] table.

4.  Complete the Assessment Metric Definition form.

<table id="table_rkj_5jw_rp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display

</td><td>

Text to appear as the answer option.

</td></tr><tr><td>

Value

</td><td>

Numeric value, greater than or equal to zero, to which the answer option equates. Values determine the order in which answer options appear. See the example below.Values are also used to calculate survey results. Each metric definition for a given question must have a different **Value**.

</td></tr></tbody>
</table>5.  Click **Submit**.


## Example

On survey questionnaires, the answer options for a question appear in order from smallest to largest **Value**. For example, consider the survey question **How do you feel?** with the answer options **Good**, **Neutral**, and **Bad**. The following table shows the answer option order based on the **Value**.

|Answer option|Value|Order|
|-------------|-----|-----|
|Good|1|First|
|Neutral|3|Second|
|Bad|5|Third|

If you use survey result calculations, ensure the question **Scale definition** is set appropriately based on the answer options. In the previous example, if you want the answer option **Good** to earn the highest score, the scale definition should be **Low** because **Good** has the smallest value.

**Parent Topic:**[Survey questions](../concept/c_SurveyQuestion.md)

**Related topics**  


[Create or modify survey questions](t_CreateOrModifySurveyQuestions.md)

[Survey question data types](../reference/r_SurveyQuestionDataTypes.md)

[Survey question template](../concept/c_SurveyQuestionTemplate.md)

[Add a metric category and metric in the question bank for surveys](add-questionbank-for-survey.md)

[Change the order of survey questions](t_ChangeTheOrderOfSurveyQuestions.md)

