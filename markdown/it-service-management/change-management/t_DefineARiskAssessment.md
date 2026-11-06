---
title: Define risk assessments
description: Define the risk assessment questions, thresholds, and conditions that calculate the risk of a change request from information that the end user provides.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/change-management/t\_DefineARiskAssessment.html
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Risk assessment, Analyze change request risk and impact, Reference, Change Management, IT Service Management]
---

# Define risk assessments

Define the risk assessment questions, thresholds, and conditions that calculate the risk of a change request from information that the end user provides.

## Before you begin

Role required: itil\_admin

The [Change Management - Risk Assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/activate-change-risk-assessment.md) plugin must be active.

## About this task

You can use a series of questions to capture the risk of a change. A different assessment of the questionnaire can be defined on the change record. The assessment uses a weighted score approach for each question. The composite weighted score derived from the answer of the end user is used to calculate risk. This score is based on the thresholds associated with the risk assessment.

Change Risk Assessment is an application built on Survey and Assessment V2 architecture. While it's possible to configure multiple metric categories on this architecture, it is better not to do so to avoid errors.

You can configure multiple change Risk Assessment definitions, each with one Metric Category. The Metric Category filter must match the filter of the change Risk Assessment condition.

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Administration** &gt; **Risk Assessments**.

2.  Select **New**.

3.  On the form, fill in the fields.

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

Conditions that determine whether a risk assessment is attached to the change. Typically, the first assessment that matches the conditions is attached during evaluation. When you define multiple questionnaires, make sure that the conditions attach the correct assessment. **Note:** Keep the conditions simple and mutually exclusive so that the assessment conditions are easy to understand and maintain.

</td></tr></tbody>
</table>4.  Open the form context menu and select **Save**.

    The page refreshes with the **Assessment Categories** and **Assessment Thresholds** related lists. The **Assessment Categories** related list enables you to define the questions that the end user answers to assess the risk of a change request.

5.  Create an assessment question.

    1.  In the **Assessment Categories** related list, select **New**.

    2.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the assessment category.|
        |Create Stakeholders|Option that, when selected, automatically creates stakeholders for all assessable records linked to this category.|
        |Weight|Value that represents importance of this category relative to other categories. The weight is multiplied by the score of the answer to calculate the weighted score.|
        |Filter|Conditions that assessable records must meet to be evaluated by metrics in this category.|
        |Description|Description of the assessment category.|

    3.  Select **Submit**.

    4.  Open the assessment category.

    5.  In the related list, select **Assessment Metrics**.

    6.  On the form, fill in the fields.

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

Value that represents importance of this metric relative to other metrics. The weight is multiplied by the score of the answer to calculate the weighted score.

</td></tr><tr><td>

Order

</td><td>

Order of the question in the assessment.

</td></tr><tr><td>

Active

</td><td>

Option that, when selected, makes the metric available for assessments and result calculations.

</td></tr><tr><td>

Mandatory

</td><td>

Option that, when selected, makes the question mandatory in an assessment.

</td></tr><tr><td class="sub-head" colspan="2">

General

</td></tr><tr><td>

Question

</td><td>

Question that is displayed on the assessment.

</td></tr><tr><td>

Description

</td><td>

Tooltip text for the assessment.

</td></tr><tr><td>

Depends on

</td><td>

The condition that determines whether the metric is shown to the user.

</td></tr><tr><td>

Allow Additional Information

</td><td>

Option that, when selected, displays a text box where the user can enter more information for the question.

</td></tr><tr><td class="sub-head" colspan="2">

Field Type

</td></tr><tr><td>

Data type

</td><td>

The data type of the answer that is given by a user for a question. **Note:** Depending on the data type that you select, additional fields might appear.

</td></tr></tbody>
</table>    7.  Select **Submit**.

    8.  In the **Assessment Threshold** related list, select **New**.

    9.  On the form, fill in the fields.

<table id="table_mwy_nc3_3w"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Risk Assessment

</td><td>

Name of the assessment that the threshold applies to.

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
</table>    10. Select **Submit**.

    **Note:** You can create or edit the assessment questionnaire through the Assessment Designer module or by selecting the **Edit in Assessment Designer** related link.

    For example, after you define the risk assessment, this is how the risk assessment score is calculated and set.

    -   **asmt\_metric\_result** stores the score set.
    -   The weight is calculated as `sum (asmt_metric_result.normalized_value)` where `asmt_metric_result.normalized_value = actual_value * weight`.
    -   The risk is calculated as `sum(actual_value * weight) > threshold`. For example, if the result is 7 and the moderate threshold is 6, the risk is moderate.

**Parent Topic:**[Risk assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/c_RskAsmtCalc.md)

**Related topics**  


[Perform risk assessment]()

