---
title: Quizzes
description: Quizzes are questionnaires that you can assign to one or more users to assess their knowledge of any subject. The quiz functionality is built on the assessment engine and provides many of the same features as assessments and surveys.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Quizzes

Quizzes are questionnaires that you can assign to one or more users to assess their knowledge of any subject. The quiz functionality is built on the assessment engine and provides many of the same features as assessments and surveys.

Each question is scored, and the overall score indicates the percentage of questions the user answered correctly. A quiz may have categories of questions that are assigned only to some users. You can assign weighting values to individual questions or categories of questions that make them more or less important when calculating the overall score. Quizzes require activation by a system administrator.

The difference between assessments, surveys, and quizzes, and when to use each; also provides a quick look at the three stages in the survey process: designing, sharing, and evaluating.

-   An administrator can create a quiz for any purpose and assign it to a single user or multiple users.
-   A quiz can contain one or more categories of questions. Each category can be assigned to users who answer only the questions in that category.
-   The system can send email notifications to these users:
    -   Recipients: The recipient can receive notification of an assigned quiz, a quiz whose allowed duration is at 50%, and a quiz that is overdue.
    -   Recipient's manager: The recipient's manager can receive notification when a quiz is overdue.
    -   Quiz manager: The quiz manager can receive notification of an overdue quiz that is assigned to them.
-   Quizzes can contain questions that are scored or not scored. Unscored questions assess opinions or involve dates and are not counted in the final score. Scored questions specify correct answers and are scored either as 0% or 100%. You can apply a weighting scale to scored questions to establish their relative importance. You can designate questions with these data types as scored questions:
    -   Checkbox
    -   Choice
    -   Duration
    -   Likert Scale
    -   Numeric Scale
    -   Template
    -   Yes/No
-   A quiz question can be dependent on the response to any scored question. For example, you can create a dependent question requesting additional information that appears only if a recipient answers No to a specific question.

## Important terms

The quiz application involves several terms.

<table id="table_xvl_ndz_fcb"><tbody><tr><td>

Quizzes

</td><td>

A quiz contains information such as duration, state, and notification controls and lists the existing categories. Text fields on the quiz form allow an administrator to create introductory content and end notes that are displayed to the recipient.

</td></tr><tr><td>

Categories

</td><td>

A quiz category represents a theme for quiz questions. Each category contains one or more questions and names the recipients for the questions in that category. By default, the system creates one category with the same name as the quiz. You can create additional categories as needed. Categories can be weighted higher or lower to determine the importance of that category in the overall score.

</td></tr><tr><td>

Questions

</td><td>

A quiz question is a question configured for a category and sent only to the users for that category. Questions have a wide variety of data types and can be individually weighted higher or lower. Questions may be scored or unscored.

</td></tr><tr><td>

Category user

</td><td>

A category user is the recipient of questions for a specific category. You can select different users to answer the questions for each category.

</td></tr><tr><td>

Templates

</td><td>

A template is a question data type that provides reusable rating scales for answers to questions. For example, the answer template named Satisfaction contains a satisfaction scale ranging from Very Satisfied to Very Dissatisfied.

</td></tr></tbody>
</table>## Quiz roles

The Quizzes application uses these roles. No role is required to take quizzes that are assigned to you.

<table id="table_tqt_b5t_hp"><thead><tr><th>

Role Title \[Name\]

</th><th>

Role Description

</th></tr></thead><tbody><tr><td>

assessment administrator \[assessment\_admin\]

</td><td>

Can administer the Assessments application and all quiz records. Can access all the modules of the Assessments application. **Note:** The itil\_admin role and the survey\_admin role contain the assessment\_admin role

</td></tr><tr><td>

Administrator \[admin\]

</td><td>

Can access all aspects of the assessment and survey processes. Only administrators can modify survey notifications, create survey modules, and import surveys.

</td></tr></tbody>
</table>-   **[Using Quizzes](using-quizzes.md)**  
You can use quizzes.
-   **[Quizzes reference](quizzes-reference.md)**  
Reference topics provide additional information about the forms, fields, and properties you use while working with quizzes.

**Parent Topic:**[Assessments and Surveys](assessments-surveys-landing-page.md)

**Related topics**  


[Assessment metrics](c_AssessmentMetrics.md)

