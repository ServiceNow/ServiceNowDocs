---
title: Create quiz questions
description: Create multiple questions for each category. Each question can be associated with only one category.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create a quiz, Quiz designer, Using Quizzes, Quizzes, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create quiz questions

Create multiple questions for each category. Each question can be associated with only one category.

## Before you begin

Role required: assessment\_admin or admin

## About this task

The [data type](../concept/c_QuizDesigner.md) that you select for each question determines how it can be answered by quiz recipients.

You can designate questions to be scored. Only scored questions are shown in the quiz results and considered when calculating the category results. You must also specify a correct answer for scored questions.

**Note:**

To designate a question as scored, you must use Assessment forms. For instructions, see [Configure a scored question](t_ConfigureAScoredQuestion.md).

## Procedure

1.  In the Design view, drag a data type icon from the Controls palette and drop it into a category container.

    ![Quiz designer drag and drop](../images/QuizDesignerDragDrop.png)

2.  Configure the question.

    **Note:** To add a question with the same data type as an existing question in the category, select the **+** in the title bar of the existing question.

    1.  Select in the gear icon in its title bar.

        ![Quiz designer question properties](../images/QuizDesignerQuestionProp.png)

    2.  On the Properties form, fill in the fields.

        For a description of the field values, see [Question Properties form](../reference/question-property-form.md).

    3.  Create any special conditions that must be met for a question to appear on the quiz by selecting the **Dependency** tab and filling in the fields.

        Dependent questions appear on the quiz when a recipient selects a specific answer or combination of answers to another question in the same category.

    4.  Select a question in the Displayed when field.

        The system selects the appropriate operator and displays the possible answers for the selected question.

    5.  Select the answers that satisfy the condition.

        Selected answers are indicated by a check mark.

        ![Quiz designer dependency](../images/QuizDesignerDependency.png)

    6.  Select **X** to close the question properties dialog box and save your settings.

3.  Drag questions to change their order within a category or move them between categories.

4.  Delete a question by selecting the X in its title bar.


**Parent Topic:**[Create a quiz](t_CreateaQuiz.md)

