---
title: Properties form
description: Description of the field values for the Properties form of survey designer.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Reference, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Properties form

Description of the field values for the Properties form of survey designer.

<table id="table_bmb_svh_br"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Concise name of the question. The system uses this value to identify the question in Assessment Metric lists and in scorecard charts.

</td></tr><tr><td>

Question

</td><td>

Text to display as the question on surveys. Enter a clear, straightforward question that is easy to understand.

</td></tr><tr><td>

Type

</td><td>

Data type selected for this question. See the table in [Controls](../concept/c_SurveyDesignerElements.md#fig_wcx_pb3_br) for the available data types.

</td></tr><tr><td>

Active

</td><td>

Check box that determines whether this question is available on a survey. A question does not appear on surveys that are generated after the question becomes inactive.

</td></tr><tr><td>

Mandatory

</td><td>

Check box to require users to answer the question. Mandatory questions are denoted by a red field status indicator and must be answered before the survey can be submitted. This field is available when the question does not have a dependency and the question type is not **Boolean** with a check box option.

</td></tr><tr><td>

Allow Additional Information

</td><td>

If selected, the **Additional Information Label** field is enabled. The **Additional Information Label** field value is displayed as a field on the survey response page to provide additional information for a question.**Note:** This is not applicable for the String and Template data types.

</td></tr><tr><td>

Boolean option

</td><td>

Whether a check box or a **Yes/No** list appears as the option for a Boolean question.

</td></tr><tr><td>

String option

</td><td>

Setting for the appearance of a string field in a question. This field is available when the question type is **String**. The string options include the following. -   **Single line**: Single-line text field 40 characters in length that allows strings of any length.
-   **String line wide**: Full page width text field that allows a single-line entry of any length.
-   **Multiline**: Full page width multiline text field that allows word wrap and returns

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

Check box for including **Not Applicable** as an option for this question. Users can select **Not Applicable** if they do not have sufficient information to respond to a question. User responses of **Not Applicable** are excluded from results calculations. This field is available when the question does not have a dependency and the question type is not **Boolean** with a check box option.

</td></tr><tr><td>

Randomize answers

</td><td>

Check box for displaying answer options in a random order. Answer preference is sometimes influenced by the order in which options appear, which can result in biased results. Randomizing options can help prevent this bias. **Note:** Randomizing options for certain questions may make those questions confusing for users. In general, only randomize options that do not follow a logical order.

</td></tr><tr><td>

Positive indicator

</td><td>

Setting that determines whether smaller or larger numerical values equate to a good score in result calculations. Select **Low values** if smaller numerical values are better, such as for a question that measures the number of incidents for a vendor. Select **High values** if larger numerical values are better, such as for a question that measures user satisfaction on a scale of one to five.

</td></tr><tr><td>

Source Field

</td><td>

Source table field that appears as a dynamic value for the question in a triggered survey. When this field value is selected, a **$\{param\}** placeholder is added at the end of the question label.**Note:** You can move this placeholder anywhere in the question label.

 When a user takes the survey, the question with dynamic value is included in the survey instance and **$\{param\}** placeholder is replaced with the source field value.

 If the record table specified in the trigger condition does not match the source table specified for the survey, or if the system fails to get the dynamic value from the source record, the **$\{param\}** placeholder is not replaced by any value and is displayed as is in the question.

For example, if the survey is triggered from a **PRB** record and the survey question is configured with a dynamic value from **Incident**, the **$\{param\}** placeholder in the survey question label is not replaced by any dynamic value and is displayed as is.When survey questions are translated to other languages by a survey admin, the **$\{param\}**placeholder should not be translated.

</td></tr><tr><td>

Allow Sentiment Analysis

</td><td>

Includes this question for the sentiment analysis of a survey.**Note:** This field is available only for String type questions.

</td></tr><tr><td>

Details

</td><td>

Information about the question that is displayed on the survey. Include details that help users understand how to answer the question.

</td></tr><tr><td>

Choices

</td><td>

Options for a question with a data type of **Choice** or **Scale**. The system automatically adds text and values that you can edit for each option. You must have at least two options, and each option must have a unique value.Click the **+** icon to add an option, or click the **X** icon to delete an option. By default, the system arranges options in the order established by their values. To change the order, drag and drop the options.

**Note:** Value numbers also contribute to the calculations of survey response scores, which can be used by advanced survey administrators.

 ![Survey designer question choice values](../image/SurveyDesignerChoiceValue.png)

</td></tr></tbody>
</table>**Parent Topic:**[Surveys reference](survey-reference.md)

