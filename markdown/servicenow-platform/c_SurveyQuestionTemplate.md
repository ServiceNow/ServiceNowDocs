---
title: Survey question template
description: Question templates define reusable sets of answer options for survey questions.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Survey questions, Survey administration, Use surveys, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Survey question template

Question templates define reusable sets of answer options for survey questions.

Question templates define reusable rating scales for answering questions, where each answer option on the scale is a template definition. For example, the template named **Satisfaction** represents a satisfaction scale and contains the following template definitions: **Very Satisfied**, **Satisfied**, **Neutral**, **Dissatisfied**, and **Very Dissatisfied**.

![Template definition](../image/TemplateDefinition.png "Template definition")

Templates are available for survey questions that have **Data type** set to **Template**. The following question templates are available in the base system. You can create or update a template as described in [Create a survey question template](../task/t_CreateASurveyQuestionTemplate.md).

|Name|Template definitions|
|----|--------------------|
|Amount|None, Few or little, Average amount, Many, Quite a lot|
|Complexity|Very Complex, Complex, Moderate, Simple, Very Simple|
|Frequency|Never, Seldom, Sometimes, Most of the time, All of the time|
|Likert 5|Strongly Disagree, Disagree, Neutral, Agree, Strongly Agree|
|Quality|Very Poor, Poor, Average, Good, Very Good|
|Satisfaction|Very Dissatisfied, Dissatisfied, Neutral, Satisfied, Very Satisfied|
|Size|Very Small, Small, Average, Large, Very Large|

-   **[Create a survey question template](../task/t_CreateASurveyQuestionTemplate.md)**  
You can create and administer question templates.
-   **[Update min and max values to match templates](../task/t_UpdateQMinAndMaxToMatchTemplates.md)**  
If you use survey result calculation data, ensure that the **Min** and **Max** values for a question that uses a template are equal to the smallest and largest template definition **Value**.

**Parent Topic:**[Survey questions](c_SurveyQuestion.md)

**Related topics**  


[Create or modify survey questions](../task/t_CreateOrModifySurveyQuestions.md)

[Survey question data types](../reference/r_SurveyQuestionDataTypes.md)

[Add a metric category and metric in the question bank for surveys](../task/add-questionbank-for-survey.md)

[Create or modify answer options](../task/t_CreateOrModifyAnswerOptions.md)

[Change the order of survey questions](../task/t_ChangeTheOrderOfSurveyQuestions.md)

