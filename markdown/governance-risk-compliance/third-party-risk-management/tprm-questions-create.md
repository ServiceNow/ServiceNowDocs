---
title: Define a question
description: After you add a question to a question bank, you can reuse it in any assessment by dropping it into the assessment. You can create custom questions, add existing questions, or add and customize the sample questions that are included with the base system.
locale: en-US
release: zurich
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 11
breadcrumb: [Classic assessments, Configure, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Define a question

After you add a question to a question bank, you can reuse it in any assessment by dropping it into the assessment. You can create custom questions, add existing questions, or add and customize the sample questions that are included with the base system.

## Before you begin

Role required: admin or sn\_vdr\_risk\_asmt.vendor\_risk\_manager

## About this task

<table id="table_om1_swv_szb"><thead><tr><th>

Term

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Metric or Assessment metric

</td><td>

A single question within a questionnaire template.

</td></tr><tr><td>

Metric type or Assessment metric type

</td><td>

A questionnaire template.

</td></tr><tr><td>

Category or Assessment category

</td><td>

A set of related questions within a questionnaire template.**Note:** There can be multiple categories within a metric type.

</td></tr></tbody>
</table>Selecting the scored option \(**Scored** check box\) is optional. All question responses unless otherwise stated are scored. The scored option changes the scoring behavior. When the 'Scored' option is selected, the score is always 0 or 100 reflecting whether the answer is correct or incorrect, and the questionRating and questionPercentContribution formulae are not used; the Normalized Value is directly set to 0 or 100. When the 'Scored' check box is not selected, the score is calculated using the questionRating and questionPercentContribution formulae to determine the Normalized Value. Selecting the Maximum normalization input field only applies when the 'Scored' check box is not selected, as it is used to define the maximum value for normalization, and the score can vary based on the input values and weights. If the 'Scored' check box is selected, the Maximum normalization input field does not apply, and the Normalized Value is simply 0 or 100. For more information on scoring and normalized scores, see [Scoring calculations using the classic assessment engine](../../grc-vendor-risk/concept/vendor-ratings-scoring.md) and [Normalize the scores for metrics](../concept/set-max-norm-input.md).

## Procedure

1.  Define or select the assessment category that is appropriate for the question that you plan to add.

    -   To select an existing assessment category, navigate to **All** &gt; **Third-party Risk Management** &gt; **Administration** &gt; **Question Bank**, and then select it in the list.
    -   For instructions on defining an assessment category, see [Set up and maintain a question bank](tprm-question-bank-create.md).
2.  Create an assessment metric \(a question\).

    In the Assessment Metrics related list for the assessment category, select **New** and then fill in the form.

<table id="table_FloorForm"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A name for the assessment metric.

</td></tr><tr><td>

Mandatory

</td><td>

Indicates whether the question must be answered.

</td></tr><tr><td>

Weight

</td><td>

A numerical value used to compare the importance of this metric to other metrics.**Note:** Weight values must be whole integers. Using decimals results in incorrect scores. For example, use 56 and not 0.56.

</td></tr><tr><td>

Category

</td><td>

The category to which the metric is associated.

</td></tr><tr><td>

Question

</td><td>

The question to be displayed on the questionnaire.

</td></tr><tr><td>

Description

</td><td>

Tooltip text to help the third-party contact better understand the question.

</td></tr><tr><td>

Details

</td><td>

An expanded description for the question that is displayed to the assessment taker. The details can include text, images, video, and links to external websites or other content.**Note:** You can define the details at the assessment level or at the category level.

</td></tr></tbody>
</table>3.  Select the **General** tab and then fill in the values.

<table id="table_dyb_xfg_vpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Method

</td><td>

The method used for gathering data for the metric.-   Assessment
-   Default answer from field
-   Default answer from script
-   Script


</td></tr><tr><td>

Order

</td><td>

Order that the question will be displayed in the questionnaire. Questions with lower values for **Order** appear earlier in the questionnaire.

</td></tr><tr><td>

Active

</td><td>

Activates the metric for assessments and results calculations.

</td></tr><tr><td>

Depends on

</td><td>

The identifier for a separate metric \(question\). The answer to the question that is specified in this field determines whether the question that you’re currently defining is displayed to the user.

 This field appears only if you select **Assessment** in the **Method** field.

</td></tr><tr><td>

Default answer

</td><td>

The field from which the default answer for the question comes.

 This field appears only if you select **Default answer from field** in the **Method** field.

</td></tr><tr><td>

Ask question

</td><td>

Specifies whether the question requires an answer when a default value is provided.

 This field appears only if you select **Default answer from field** or **Default answer from script** in the **Method** field.

</td></tr><tr><td>

Script

</td><td>

The scripts used to produce performance indicators for the associated metric when the assessment is generated.

 This field appears only if you select **Default answer from script** or **Script** in the **Method** field.

 **Note:** To enter a tab character in your script, use the **Tab** key. For tab actions, press **Esc** to tab forward and **Shift+Esc** to tab backward.

</td></tr></tbody>
</table>4.  Select the **Question Type** tab and then fill in the form.

    **Note:** The fields that appear depend on the **Data type** that you select.

<table id="table_jkh_gtr_z4"><thead><tr><th>

Data type

</th><th>

Description and additional fields

</th></tr></thead><tbody><tr><td>

Attachment

</td><td>

On questionnaires, users attach one or more files to a question.

 This question type is not scored by default.

</td></tr><tr><td>

Check box

</td><td>

On questionnaires, users select a check box for a statement or leave it cleared.

 To define a single metric to be scored for the data type, select **Scored** and select a **Correct answer** for the question.

 If you didn’t select the **Scored** check box, set the **Scale definition**. If a selected check box equates to a good score, set the field to **High**. If a small numerical value should be interpreted as a positive score, set the field to **Low**.

</td></tr><tr><td>

Choice

</td><td>

On questionnaires, users select a value from a list of custom answer options. Create a metric definition for each answer option.**Note:** If you use a comma in one of the answer options, they will appear as a hyphen when the questionnaire is exported as a spreadsheet. For example, if "Yes, add more info" is one of your answer options, it appears as "Yes- add more info" in an exported spreadsheet.

Select the **Randomize answers** check box to randomize the order of answer options for a question.

Select the **Reference table** to use for reference data type questions.

Define conditions to restrict choices to those that meet the selection criteria.

To define a single metric to be scored for the data type, select **Scored** and then select a correct answer for the question.

If you didn’t select the **Scored** check box, set the **Scale definition** value.

-   If a selected check box is a good score, set to **High**.
-   If a small numerical value is a good score, set to **Low**.
You can select the **Maximum Normalization input** check box to calculate assessment scores for questions using a normalization input value. For more information, see [Normalize the scores for metrics](../concept/set-max-norm-input.md).

</td></tr><tr><td>

Date

</td><td>

On questionnaires, users select a date.This question type is not scored by default.

</td></tr><tr><td>

Date/Time

</td><td>

On questionnaires, users select a date and time.This question type is not scored by default.

</td></tr><tr><td>

Duration

</td><td>

On questionnaires, users specify an answer that falls within the **Min**/**Max** range.Select the **Dependent plugin** that the duration depends upon:

-   Asset Management
-   CMDB
-   Core
-   Cost Management
-   Procurement
-   Software Asset Management
To define a single metric to be scored for the data type, select **Scored** and select a **Correct answer** for the question.

If you didn’t select the **Scored** check box, set the **Scale definition**.

-   If a large numerical value is a good score, set the field to **High**.
-   If a small numerical value is a positive score, set the field to **Low**.


</td></tr><tr><td>

Image Scale

</td><td>

On questionnaires, users select an image scale.

 To define a single metric to be scored for the data type, select **Scored** and select a **Correct answer** for the question. You must unlock the **Correct answer** field to make changes.

 If you didn’t select the **Scored** check box, set the **Scale definition**.

-   If a large numerical value is a good score, set to **High**.
-   If a small numerical value is a good score, set to **Low**.


</td></tr><tr><td>

Likert Scale

</td><td>

On questionnaires, users select a value from a custom scale of answer options. Create a metric definition for each answer option, which is represented by a selection button on the scale. A Likert scale metric that evaluates an application's ease of use might have **Easy**, **Average**, and **Difficult** metric definitions.Select **Randomize answers** to randomize the order of answer options for the question.

To define a single metric to be scored for the data type, select **Scored** and select a **Correct answer** for the question. You must unlock the **Correct answer** field to make changes.

If you didn’t select the **Scored** check box, set the **Scale definition**.

-   If a large numerical value is a good score, set to **High**.
-   If a small numerical value is a good score, set to **Low**.


</td></tr><tr><td>

Multiple Selection

</td><td>

On questionnaires, users select one or more values from a list of custom answer options. For the **Multiple Selection** data type, you have the option to specify a **Reference table** and conditions that filter, which values from the table are displayed in the list.For example, if you select **Country \[core\_country\]** as the reference table and set the conditions as **Name** + **starts with** + **B**, the query returns only the 19 countries that start with the letter B, instead of the full list of 231 countries.

To define a single metric to be scored for this data type, select **Scored** and select a **Correct answer** for the question. You must unlock the **Correct answer** field to make changes.

If you didn’t select the **Scored** check box, set the **Scale definition**.

-   If a large numerical value is a good score, set to **High**.
-   If a small numerical value is a good score, set to **Low**.
You can select the **Maximum Normalization input** check box to calculate assessment scores for questions using a normalization input value. For more information, see [Normalize the scores for metrics](../concept/set-max-norm-input.md).

</td></tr><tr><td>

Number

</td><td>

On questionnaires, users enter a number that falls within the **Min**/**Max** range.To define a single metric to be scored for this data type, select **Scored** and select a **Correct answer** for the question.

If you didn’t select the **Scored** check box, set the **Scale definition**.

-   If a large numerical value is a good score, set to **High**.
-   If a small numerical value is a good score, set to **Low**.


</td></tr><tr><td>

Numeric Scale

</td><td>

On questionnaires, users enter a number that falls within the **Min**/**Max** range.To define a single metric to be scored for this data type, select **Scored** and select a **Correct answer** for the question.

If you didn’t select the **Scored** check box, set the **Scale definition**.

-   If a large numerical value is a good score, set to **High**.
-   If a small numerical value is a good score, set to **Low**.


</td></tr><tr><td>

Percentage

</td><td>

On questionnaires, users enter a percentage number that falls within the **Min**/**Max** range.To define a single metric to be scored for this data type, select **Scored** and select a **Correct answer** for the question.

If you didn’t select the **Scored** check box, set the **Scale definition**.

-   If a large numerical value is a good score, set to **High**.
-   If a small numerical value is a good score, set to **Low**.


</td></tr><tr><td>

Ranking

</td><td>

On questionnaires, users can select a different order number for each option to rank them. A user can either fill in the number or drag an option.Select **Randomize answers** to randomize the order of answer options for the question.

Set the **Scale definition**.

-   If a large numerical value equates to a good score, set the field to **High**.
-   If a small numerical value should be interpreted as a positive score, set the field to **Low**.


</td></tr><tr><td>

Reference

</td><td>

On questionnaires, users select a value from a list that is generated from a specified **Reference table**. For example, a user could select a user name in response to a question if you specify User \[sys\_user\] as the reference table. You also have the option of defining conditions for limiting the information pulled from the reference table into manageable chunks.

</td></tr><tr><td>

String

</td><td>

On questionnaires, users enter text. The size of the string field depends on the **String option** you select:

-   Single line
-   Single line wide
-   Multiline
 This question type is not scored by default.

</td></tr><tr><td>

Template

</td><td>

On questionnaires, users select a value from a predefined series of answer options. There must be at least one template defined to use this data type. For a template, there’s a template definition for each answer option, which is represented by a radio button.To define a single metric to be scored for this data type, select **Scored** and select a **Correct answer** for the question. You must unlock the **Correct answer** field to make changes.

If you didn’t select the **Scored** check box, set the **Scale definition**.

-   If a large numerical value is a good score, set to **High**.
-   If a small numerical value is a good score, set to **Low**.


</td></tr><tr><td>

Yes/No

</td><td>

On questionnaires, users select **Yes** or **No** from a list.

 To define a single metric to be scored for this data type, select **Scored** and select a **Correct answer** for the question.

 If you didn’t select the **Scored** check box, set the **Scale definition**.

-   If a **Yes** answer is a good score, set to **High**.
-   If a **No** answer is a good score, set to **Low**.


</td></tr></tbody>
</table>5.  Select **Update** to save the questions to the question bank.


