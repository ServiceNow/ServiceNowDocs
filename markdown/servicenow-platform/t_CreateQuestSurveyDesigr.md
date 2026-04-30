---
title: Create a question in the survey designer
description: You can create multiple questions for each category in the survey designer, but each question can only be associated with one category.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Survey designer, Survey administration, Using surveys, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a question in the survey designer

You can create multiple questions for each category in the survey designer, but each question can only be associated with one category.

## Before you begin

Role required: admin or survey\_admin

## About this task

The data type that you select for each question determines how it can be answered by survey recipients.

## Procedure

1.  In the Design view, drag a data type icon from the Controls palette and drop it into a category container.

2.  To configure the question, click the gear icon in its title bar.

    The Properties dialog box opens.

3.  On the Properties form, fill in the fields.

    For a description of the field values, see [Properties form](../reference/properties-form-survey-designer.md).

4.  To create any special conditions that must be met before the question appears on the survey, click the Dependency tab.

    The question must have a data type of **Boolean**, **Choice**, **Scale**, or **Template**.

    For example, the question, “How many states have you visited in India”, is a dependent question for the current question “Have you visited any other state in India?”. The dependent question appears exactly below the current question only if your answer satisfies the condition in the current question. If not, the dependent question does not appear anywhere in the survey.

5.  Select a question in the **Displayed when** field.

    The system selects the appropriate operator and displays the possible answers for the selected question.

6.  Select the answer that satisfies the condition.

    You can select more than one answer. Selected answers are indicated by a check mark.

    The system prevents recursive dependencies between questions. For example, if Question A depends on Question B, Question B cannot depend on Question A.

7.  Click the **X** icon to close the question properties dialog box and save your settings.

8.  To add a question with the same data type as an existing question in the category, click the **+** icon in the title bar of the existing question.

9.  Drag and drop questions to change their order within a category or move them between categories.

10. To delete a question, click the **X** icon in its title bar.


**Parent Topic:**[Survey designer](../concept/c_SurveyDesigner.md)

**Related topics**  


[Survey designer elements](../concept/c_SurveyDesignerElements.md)

[Configure a survey in the survey designer](t_ConfigSurveyInSurveyDesgnr.md)

[Survey categories](../concept/c_SurveyCategory.md)

[Survey question data types](../reference/r_SurveyQuestionDataTypes.md)

[Create custom metric type](create-custom-templates-questions.md)

[Edit a survey in the survey designer](t_EditASurveyInTheSurveyDesigner.md)

[Configure category weights for a survey](t_ConfigCatWeightsForSurvey.md)

[Survey question template](../concept/c_SurveyQuestionTemplate.md)

[Create a survey designer template question](t_CreateASurveyDesignerTemplateQ.md)

