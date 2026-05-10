---
title: Configure a scored question
description: Only scored questions are considered when calculating category and quiz results.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a quiz, Quiz designer, Using Quizzes, Quizzes, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure a scored question

Only scored questions are considered when calculating category and quiz results.

## Before you begin

Role required: assessment\_admin or admin

## About this task

A question must have a correct answer specified to be scored. Only results for scored questions are displayed in the [quiz scorecard](../concept/c_QuizScorecards.md).

## Procedure

1.  Navigate to **All** &gt; **Quizzes** &gt; **Quizzes**.

2.  Open the quiz containing the questions you want to mark as scored.

3.  In the **Metric Categories** related list on the **Assessment Metric Type** form, select the category for the questions you want to mark as scored.

4.  In the **Assessment Metrics** related list on the **Metric Category** form, select a question from the list.

5.  In the **Question Type** section of the **Assessment Metric** form, select the **Scored** check box.

    This check box is not available if the question's data type is not supported for scoring.

6.  Select the **Correct answer** for the question.

    **Note:** Multiple correct answers are supported for a few data types. See [Data types for quizzes](../reference/r_AvailableDataTypes.md).

7.  Click **Update**.

8.  Repeat the process for all the questions in the category that you want the system to score.

9.  Return to the list of metric categories, select another category, and configure scoring for the appropriate questions in that category.


**Parent Topic:**[Create a quiz](t_CreateaQuiz.md)

**Parent Topic:**[Edit a quiz](t_EditaQuiz.md)

