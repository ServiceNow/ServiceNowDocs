---
title: Survey Question form
description: Description of the field values for the Survey Question form.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Reference, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Survey Question form

Description of the field values for the Survey Question form.

<table id="table_kmc_dqv_rp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the question. When you create a survey, the question name is the same as the text in the **Question** field.

</td></tr><tr><td>

Question

</td><td>

Text to use for the question, which appears on survey questionnaires.

</td></tr><tr><td>

Data type

</td><td>

Data type of the question. The fields for the response depend on the data type.**Note:** If another question depends on this question, you cannot change the data type.

</td></tr><tr><td>

Template

</td><td>

Question template to use for the answer options.This field is visible and required only if the data type is **Template**.

 **Note:** If another question depends on this question, you cannot change the template.

</td></tr><tr><td>

Scale definition

</td><td>

Setting that determines whether smaller or larger numerical values equate to a good score in result calculations. Select **Low** if smaller numerical values are better, such as for a question that measures the number of incidents for a vendor. Select **High** if larger numerical values are better, such as for a question that measures user satisfaction on a scale of one to five.This field is visible and required only when certain data types are selected.

</td></tr><tr><td>

Randomize answers

</td><td>

Check box that determines whether to present the answer options for this question in a random order each time a user opens the survey. Answer preference is sometimes influenced by the order in which answer options appear, which can result in biased results. Randomize answer options to help prevent this bias.This field is visible only if the data type is **Choice** or **Likert Scale**.

 **Note:** Randomizing answer options may make a question confusing. In general, only randomize answer options that do not follow a logical order.

</td></tr><tr><td>

Mandatory

</td><td>

Check box that makes the question mandatory \(selected\) or optional \(cleared\) on survey questionnaires. Users cannot submit questionnaires until they provide valid responses to all mandatory questions, which are denoted by a red field status indicator.This field is visible only when the **Depends on** field is empty and the data type is not **Checkbox**. Questions that depend on other questions and check box questions cannot be mandatory.

</td></tr><tr><td>

Allow not applicable

</td><td>

Check box that determines whether to include a **Not Applicable** answer option for this question on survey questionnaires. User responses of **Not Applicable** are excluded from results calculations.This field is visible only if the data type is **Choice**, **Likert Scale**, **Template**, or **Yes/No**.

</td></tr><tr><td>

Allow Additional Information

</td><td>

If selected, the **Additional Information Label** field is enabled. The **Additional Information Label** field value is displayed as a field on the survey response page to provide additional information for a question.**Note:**

-   This is only available on the Service Portal and is not supported on the Platform or Mobile views.
-   This is not applicable for the String and Template data types.

</td></tr><tr><td>

Depends on

</td><td>

Setting used to make this a conditional question, meaning that it only appears when users answer another question a certain way. To make a question depend on another question, select an existing question from the list, which displays **Checkbox**, **Choice**, **Template**, and **Yes/No** questions of the same category as this question. Then, use the **Displayed when** field to set the conditions that cause this question to appear on surveys.

 The system prevents the creation of recursive dependencies between questions. For example, if Question A depends on Question B, Question B cannot depend on Question A.

</td></tr><tr><td>

Displayed when

</td><td>

Answer options for the selected **Depends on** question which, when chosen on surveys, display this question. This field is visible and required only when the **Depends on** field is set.

</td></tr><tr><td>

Min

</td><td>

Smallest numerical value to be used as an answer option for this question. This field is visible and required only if the data type is **Choice**, **Likert Scale**, **Number**, or **Percentage**.

</td></tr><tr><td>

Max

</td><td>

Largest numerical value to be used as an answer option for this question. This field is visible and required only if the data type is **Choice**, **Likert Scale**, **Number**, or **Percentage**.

</td></tr><tr><td>

String option

</td><td>

Selection that determines what kind of response text box appears for this question on survey questionnaires. This field is visible and required only if the data type is **String**.

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

Condition

</td><td>

Condition to filter the reference records from the table specified in the **Reference** field.**Note:** This field appears only for the Reference metric type.

</td></tr><tr><td>

Field validation

</td><td>

Validate the value entered for a String type metric of a survey. Possible validations are:-   Email
-   IP Address\(IPV4,IPV6\)
-   Phone Number \(E.164\)
-   URL

 **Note:** This field appears only for the String metric type.

</td></tr><tr><td class="sub-head" colspan="2">

Related Lists

</td></tr><tr><td>

Assessment Metric Definitions

</td><td>

Answer options for this question.This related list is available only if the **Data type** is **Choice** or **Likert Scale**.

</td></tr></tbody>
</table>**Parent Topic:**[Surveys reference](survey-reference.md)

**Related topics**  


[Create or modify survey questions](../task/t_CreateOrModifySurveyQuestions.md)

