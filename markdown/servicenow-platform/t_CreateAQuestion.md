---
title: Create questions
description: Create quiz questions. A category can have multiple questions associated with it.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Create quizzes with forms, Using Quizzes, Quizzes, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create questions

Create quiz questions. A category can have multiple questions associated with it.

## Before you begin

Role required: none

## About this task

Each question can only be associated with one category. Each question has an answer data type that determines how recipients answer the question. Questions are records in the Quiz view of the Assessment Metric table.

## Procedure

1.  Open a category record.

2.  Create a question record in one of the following ways:

    -   By accessing the Assessment Metrics related list and selecting **New**.
    -   Navigate to **Quiz Management** &gt; **Questions** and select **New**.
    **Warning:** When you create a **Choice**or **Likert Scale** question, you must reopen the Assessment Metric form after you submit it to create answers. If you distribute a questionnaire without creating the answers for questions with these data types, recipients are unable to answer the questions. If the questions are mandatory, the recipients are unable to submit their questionnaires.

    On the form, fill in the fields.

<table id="table_hpv_tc3_cr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

\[Required\] Name of the question.

</td></tr><tr><td>

Category

</td><td>

\[Required\] Category the question belongs to. The system populates this category if you create a new question from the Metric Category form.**Note:** You cannot change the category if the **Depends on** field is set or if another metric depends on this metric.

</td></tr><tr><td>

Method

</td><td>

Setting that determines how to use the question.-   **Assessment**: Makes the question available on a quiz distributed to users. The **Assessment** method is compatible with all data types except **Duration**.
-   **Script**: Queries the database without user participation. Scripted questions are of limited value for quizzes, because they do not assess a user's knowledge of a topic.
 **Note:** If you select a **Data type** that is incompatible with the selected **Method**, the system automatically changes the **Method** to the correct value.

</td></tr><tr><td>

Weight

</td><td>

Numeric value that represents the importance of this question relative to other questions in the same category. By default, the weight is 10. For weighting suggestions, see [weight categories and metrics](../concept/c_AssessmentMetrics.md). This field is available and required unless the **Data type** is **Date**, **Date/Time**, or **String**. These data types are not included in results calculations.

</td></tr><tr><td>

Order

</td><td>

\[Required\] Numeric value that determines the order of the question in the category. The question with the smallest order value appears as the first question in the category's section. By default, the order is 100. **Note:** It does not matter which order value you use for metrics with the **Script** method, because they do not appear on questionnaires.

</td></tr><tr><td>

Active

</td><td>

Check box that determines whether this question appears on quizzes. If a question is inactive, it does not appear on quizzes generated after the question becomes inactive.

</td></tr><tr><td>

Mandatory

</td><td>

Check box for requiring users to answer the question. Users cannot submit questionnaires until they provide valid responses to all mandatory questions, which are denoted by a red field status indicator.This field is available only if the **Method** is **Assessment**, the **Depends**on field is empty, and the **Data type** is not **Checkbox**.

</td></tr><tr><td>

Allow not applicable

</td><td>

Check box for including **Not Applicable** as a possible answer for this question. Users can select **Not Applicable** if they do not have sufficient information to respond to a question. User responses of **Not Applicable** are excluded from results.

</td></tr><tr><td class="sub-head" colspan="2">

Question

</td></tr><tr><td>

Question

</td><td>

The question that is displayed in quizzes. Enter a clear, straightforward question that is easy to understand.

</td></tr><tr><td>

Details

</td><td>

Information about the question and what it evaluates. Include details that help users understand how to answer the question or when you need HTML enhanced details for your question. You can create HTML text in this field with the WYSIWYG editor, such as embedding links and images.

</td></tr><tr><td>

Depends on

</td><td>

An existing question that this question is dependent on. You can select **Checkbox**,**Choice**, **Likert Scale**, **Template**, and **Yes/No** questions from the same category as this question. Then use the Displayed when field to set the conditions for displaying this question. The system prevents the creation of recursive dependencies between questions. For example, if Question A depends on Question B, Question B cannot depend on Question A.

</td></tr><tr><td class="sub-head" colspan="2">

Question Type

</td></tr><tr><td>

Data type

</td><td>

\[Required\] Format of the expected response data. See the table of **data types** for details. **Note:** You cannot change the data type if another question depends on this question

</td></tr><tr><td>

Randomize answers

</td><td>

Check box for displaying the possible answers for this question in a random order whenever the question appears. Answer preference is sometimes influenced by the order in which answer options appear, which can result in biased results. Randomizing answer options can help prevent this bias. This check box is available only if the **Data type** is **Choice** or **Likert** Scale.**Note:** Randomizing answer options for certain questions may make those questions confusing for users. In general, only randomize answer options that do not follow a logical order.

</td></tr><tr><td>

Scale definition

</td><td>

Setting that determines whether lesser or greater numerical values equate to a good score in quiz result calculations. Select **Low** if lesser numerical values are better. Select **High** if greater numerical values are better. The default value is**High**. This field is available and required unless the **Data type** is **Date**, **Date/Time**, or **String**. The results for these data types are not included in results calculations. When the Scored check box is selected, the scale value is set to **High** and the field is hidden. **Note:** For information about how to set the scale definition for data types that do not require you to set a numerical value, see [Data types for assessments](../reference/r_DataTypes.md).

</td></tr><tr><td>

Min

</td><td>

Lowest numerical value that can be used as an answer option. This field is available and required only if **Data type** is **Number**, **Duration**, or **Percentage**.

</td></tr><tr><td>

Max

</td><td>

Highest numerical value that can be used as an answer option or scaled value. This field is available and required if **Data type** is **Number**, **Duration**, or **Percentage**.

</td></tr><tr><td>

String option

</td><td>

Setting for the appearance of a string field in a question. This field is available when the question type is **String**. The string options are:-   **Single line**: Single line text field 40 characters in length that allows strings of any length.
-   **String line wide**: Full page width text field that allows a single line entry of any length.
-   **Multiline**: Full page width multiline text field that allows word wrap and returns.


</td></tr><tr><td>

Scored

</td><td>

Check box for using answers in scoring the category results and showing them in the quiz results. Scored questions are available for these data types:-   Choice
-   Likert Scale
-   Template
-   Checkbox
-   Yes/No
Selecting this check box hides the **Scale definition** field and sets the value in that field to **High**.

</td></tr><tr><td>

Correct answer

</td><td>

\[Required\] Desired answer to a scored question. This field is available when the **Scored** check box is selected. Multiple correct answers are supported for a few data types. See [Data types for quizzes](../reference/r_AvailableDataTypes.md).

</td></tr><tr><td>

Template

</td><td>

Answer template to use with this question. This field is available when the **Data type** is **Template**.

</td></tr><tr><td class="sub-head" colspan="2">

Related List

</td></tr><tr><td>

Assessment Metric Definitions

</td><td>

List of options for this question. This related list is available only if the **Data type** is **Choice** or **Likert Scale**.

</td></tr></tbody>
</table>
**Parent Topic:**[Create quizzes with forms](../concept/c_CreateQuizzesWithForms.md)

**Related topics**  


[Assessment metrics](../concept/c_AssessmentMetrics.md)

[Create quizzes with forms](../concept/c_CreateQuizzesWithForms.md)

[Create a quiz](t_CreateaQuiz.md)

[Set up a category](t_SetUpACategory.md)

[Select a user for a category](t_SelectAUserForACategory.md)

[Data types for quizzes](../reference/r_AvailableDataTypes.md)

[Create questions](t_CreateAQuestion.md#)

