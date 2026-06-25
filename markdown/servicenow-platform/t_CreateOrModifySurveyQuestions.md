---
title: Create or modify survey questions
description: You can create and administer survey questions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/t\_CreateOrModifySurveyQuestions.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Survey questions, Survey administration, Use surveys, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create or modify survey questions

You can create and administer survey questions.

## Before you begin

Role required: admin or survey\_admin

## About this task

Changes to a survey, such as the addition of questions or the modification of question templates, do not apply immediately to the existing survey instances. However, the changes apply immediately to any new survey instances that are created after the changes are saved.

## Procedure

1.  Navigate to **All** &gt; **Survey** &gt; **View Surveys**.

2.  Open a survey definition.

3.  In the **Metric Categories** related list, open a category.

4.  In the **Assessment Metrics** related list, open an existing question or click **New**.

    Each survey question is stored as a record on the Assessment Metric \[asmt\_metric\] table with a modified view for survey use.

5.  On the Survey Question form, fill in the fields.

    The fields that appear depend on the selected **Data type**.

    For a description of the field values, see [Survey Question form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/survey-question-form.md).

6.  Save the record.

    **Note:**

    -   Be sure to create answer options if you select the **Choice** or **Likert Scale** data type.
    -   You cannot delete a survey question \(metric\) with user responses. To delete a survey question with user responses, you should delete the responses, and then delete the survey question.

**Parent Topic:**[Survey questions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/c_SurveyQuestion.md)

**Related topics**  


[Survey question data types]()

[Survey question template]()

[Add a metric category and metric in the question bank for surveys]()

[Create or modify answer options]()

[Change the order of survey questions]()

[Survey question template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/c_SurveyQuestionTemplate.md)

[Trigger condition example](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/r_TriggerConditionExample.md)

[Survey trigger conditions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/c_TriggerConditions.md)

