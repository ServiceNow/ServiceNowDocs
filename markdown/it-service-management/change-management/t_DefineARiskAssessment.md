---
title: Define risk assessments
description: Change Management - Risk Assessment provides a flexible way to capture information from the end user to calculate the risk of the associated change request. You can define the risk assessment questions, thresholds, and conditions that calculate risk for any change request.
locale: en-US
release: zurich
product: Change Management
classification: change-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Risk assessment, Analyze change request risk and impact rating, Reference, Change Management, IT Service Management]
---

# Define risk assessments

Change Management - Risk Assessment provides a flexible way to capture information from the end user to calculate the risk of the associated change request. You can define the risk assessment questions, thresholds, and conditions that calculate risk for any change request.

## Before you begin

Role required: itil\_admin

[Change Management - Risk Assessment](activate-change-risk-assessment.md) must be activated.

## About this task

You can use a series of questions to capture the risk of a change. A different assessment of the questionnaire can be defined on the change record. The assessment uses a weighted score approach for each question. The composite weighted score derived from the answer of the end user is used to calculate risk. This score is based on the thresholds associated with the risk assessment.

Change Risk Assessment is an application built on Survey and Assessment V2 architecture. While it's possible to configure multiple metric categories on this architecture, it is better not to do so to avoid errors.

You can configure multiple change Risk Assessment definitions each with one Metric Category, where the Metric Category filter is identical to the filter of the change Risk Assessment condition.

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Administration** &gt; **Risk Assessments**.

2.  Click **New**.

3.  Complete the form, as appropriate.

<table id="table_imb_vky_zp"><thead><tr><th>

Field

</th><th>

Input value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the risk assessment. This name is displayed to the end user.

</td></tr><tr><td>

State

</td><td>

The state of the assessment: **Draft** or **Published**.

</td></tr><tr><td>

Description

</td><td>

Description of the risk assessment.

</td></tr><tr><td>

Condition

</td><td>

Conditions which determines if a risk assessment is attached to the change. Typically, the first attachment that matches the conditions gets attached during evaluation. Therefore, ensure that the conditions result in the correct assessments being attached especially when defining multiple questionnaires. **Note:** Ensure that the conditions are simple and mutually exclusive so that the assessment conditions are easy to understand and maintain.

</td></tr></tbody>
</table>4.  Click the form context menu and select **Save**.

    The page refreshes with the **Assessment Categories** and **Assessment Thresholds** related lists. The **Assessment Categories** related list enables you to define the questions that the end user answers to assess the risk of a change request.

5.  Complete the following steps to create an assessment question.

    1.  In the **Assessment Categories** related list, click **New**.

    2.  Complete the form, as appropriate.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the assessment category.|
        |Create Stakeholders|If selected, automatically creates stakeholders for all assessable records linked to this category.|
        |Weight|Value that represents importance of this category relative to other categories. The weight is multiplied to the score of the answer to calculate the weighted score.|
        |Filter|Only assessable records that meet filter conditions are evaluated by metrics in this category.|
        |Description|Description of the assessment category.|

    3.  Click **Submit**.

    4.  Open the assessment category.

    5.  In the related list, click **Assessment Metrics**.

    6.  Complete the form, as appropriate.

<table id="table_bg4_3hm_2bb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the assessment metric.

</td></tr><tr><td>

Category

</td><td>

The category of the assessment metric.

</td></tr><tr><td>

Method

</td><td>

The method of gathering data for this metric.

</td></tr><tr><td>

Weight

</td><td>

Value that represents importance of this metric relative to other metrics. The weight is multiplied to the score of the answer to calculate the weighted score.

</td></tr><tr><td>

Order

</td><td>

Order of the question in the assessment.

</td></tr><tr><td>

Active

</td><td>

If selected, the metric is activated to be used for assessments and result calculations.

</td></tr><tr><td>

Mandatory

</td><td>

If selected, makes a field mandatory in an assessment.

</td></tr><tr><td class="sub-head" colspan="2">

General

</td></tr><tr><td>

Question

</td><td>

Question that is displayed on the assessment.

</td></tr><tr><td>

Description

</td><td>

Tool tip text for the assessment.

</td></tr><tr><td>

Depends on

</td><td>

The condition that determines whether the metric is shown to the user or not.

</td></tr><tr><td>

Allow Additional Information

</td><td>

If selected, a text box appears for the user to enter additional information for the question.

</td></tr><tr><td class="sub-head" colspan="2">

Field Type

</td></tr><tr><td>

Data type

</td><td>

The data type of the answer that is given by a user for a question. **Note:** Depending on the data type that you select, additional fields may appear.

</td></tr></tbody>
</table>    7.  Click **Submit**.

    8.  In the **Assessment Threshold** related list, click **New**.

    9.  Complete the form, as appropriate.

<table id="table_mwy_nc3_3w"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Risk Assessment

</td><td>

The assessment name for which assessment threshold is applied.

</td></tr><tr><td>

Risk

</td><td>

Risk value applied on the change request. **Note:** Risk value can be overridden by risk conditions.

</td></tr><tr><td>

Application

</td><td>

The name of the application that contains the record.

</td></tr><tr><td>

Score greater than

</td><td>

The threshold against which the composite score is compared and evaluated.

</td></tr></tbody>
</table>    10. Click **Submit**.

    **Note:** You can create or edit the assessment questionnaire through the Assessment Designer module or by clicking **Edit in Assessment Designer** related link.

    For example, after you define the risk assessment, this is how the risk assessment score is calculated and set.

    -   **asmt\_metric\_result** stores the score set.
    -   The weight is calculated as `sum (asmt_metric_result.normalized_value)` where `asmt_metric_result.normalized_value = actual_value * weight`.
    -   The risk calculated as `sum(actual_value * weight) > threshold`. For example, If the result is 7 and moderate threshold is 6 risk is moderate.

**Parent Topic:**[Risk assessment](../concept/c_RskAsmtCalc.md)

**Related topics**  


[Perform risk assessment](t_AssessRisk.md)

