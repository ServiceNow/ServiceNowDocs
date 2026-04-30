---
title: Question Properties form
description: Description of the field values for the Question Properties form.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Reference, Quizzes, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Question Properties form

Description of the field values for the Question Properties form.

<table id="table_bmb_svh_br"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

\[Required\] Name of the question. Create a concise and easily recognizable name for your question. The system uses this value to identify the question in Assessment Metric lists and in scorecard charts.

</td></tr><tr><td>

Question

</td><td>

Text to display as the question on quizzes. Enter a clear, straightforward question that is easy to understand.

</td></tr><tr><td>

Type

</td><td>

\[Read-only\] Data type selected for this question. See the table in [Controls](../concept/c_QuizDesigner.md) for possible data types.

</td></tr><tr><td>

Active

</td><td>

Check box that determines whether this question is available on a quiz. If a question is marked inactive, it does not appear on quizzes generated after the question becomes inactive.

</td></tr><tr><td>

Boolean option

</td><td>

Whether a check box or a **Yes/No** list appears as the option for the Boolean question.

</td></tr><tr><td>

Mandatory

</td><td>

Check box for requiring users to answer the question. Users cannot submit quizzes until they answer all mandatory questions, which are denoted by a red Introduction\_to\_Fields\#Field\_Status\_Indicator" --&gt; field status indicator. This field is available when the question does not have a dependency and the question [Controls](../concept/c_QuizDesigner.md) is not **Boolean** with a check box option.

</td></tr><tr><td>

String option

</td><td>

Setting for the appearance of a string field in a question. This field is available when the question type is **String**. The string options are: -   **Single line**: Single line text field 40 characters in length that allows strings of any length.
-   **String line wide**: Full page width text field that allows a single line entry of any length.
-   **Multiline**: Full page width multi-line text field that allows word wrap and returns.

</td></tr><tr><td>

Min

</td><td>

Lowest positive whole number that users can enter or select to answer the question. This field is available when the question type is **Number**, **Percentage**, or **Numeric Scale**.

</td></tr><tr><td>

Max

</td><td>

Highest positive whole number that users can enter or select to answer the question. This field is available when the question type is **Number**, **Percentage**, or **Numeric Scale**.

</td></tr><tr><td>

Allow not applicable

</td><td>

Check box for including **Not Applicable** as an option for this question. Users can select **Not Applicable** if they do not have sufficient information to respond to a question. User responses of **Not Applicable** are excluded from results calculations. This field is available when the question does not have a dependency and the question [data type](../concept/c_QuizDesigner.md) is not **Boolean** with a check box option.

</td></tr><tr><td>

Randomize answers

</td><td>

Check box for displaying answer options in a random order whenever the question appears in a quiz. Answer preference is sometimes influenced by the order in which options appear, which can result in biased results. Randomizing options can help prevent this bias. Randomizing options for certain questions may make those questions confusing for users. In general, only randomize options that do not follow a logical order.

</td></tr><tr><td>

Details

</td><td>

Information about the question that is displayed on the quiz. Include details that help users understand how to answer the question. You can also enter HTML text in this field with the WYSIWYG editor. For example, include HTML to embed links and images.

</td></tr><tr><td>

Correct answer

</td><td>

Answer option that you want to be selected by users. When you specify a correct answer for a question, the system scores the question. This field is available for all data types except **Date**, **Date/Time**, and **String**. Multiple correct answers are supported for a few data types. See [data types](../concept/c_QuizDesigner.md).

</td></tr><tr><td>

Choices

</td><td>

Options for a question with a data type of **Choice** or **Scale**. The system automatically adds text and values that you can edit for each option. Click the **+** icon to add an option, or click the **X** icon to delete an option. By default, the system arranges options in the order established by their values. To change the order, drag and drop the options.

</td></tr><tr><td class="sub-head" colspan="2">

Dependency

</td></tr><tr><td>

Displayed when

</td><td>

Condition builder that hides or displays the question depending on the answer to another question in the same category. Select an existing question from the list with a data type of **Boolean**, **Choice**, **Scale**, or **Template**. Create the condition that must exist for recipients to see the dependent question, using the **is** or **is one of** operator. The system prevents recursive dependencies between questions. For example, if Question A depends on Question B, Question B cannot depend on Question A.

</td></tr></tbody>
</table>**Parent Topic:**[Quizzes reference](../concept/quizzes-reference.md)

**Related topics**  


[Create quiz questions](../task/t_CreateAQuizQuestion.md)

