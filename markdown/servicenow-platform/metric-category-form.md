---
title: Metric Category form
description: Description of the field values for the Metric Category form.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Reference, Assessments, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Metric Category form

Description of the field values for the Metric Category form.

<table id="table_b2p_g5d_x4"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the metric category. The name appears on assessment questionnaires.

</td></tr><tr><td>

Type

</td><td>

\[Required\] Metric type this category is used for. Metrics in this category can be used to evaluate assessable records for the type you select. This field becomes read-only after you save the record.

</td></tr><tr><td>

Create stakeholders

</td><td>

Check box that enables \(selected\) or disables \(cleared\) automatic [stakeholder](r_CategoryUsersAndStakeholders.md) creation for this category. When the check box is selected, the system makes all associated category users stakeholders for each assessable record associated to this category. This saves the time required to manually create stakeholders. For more information, see Create Stakeholders Automatically. Existing stakeholders are not impacted if you clear the check box.

</td></tr><tr><td>

Table

</td><td>

\[Read-Only\] Table that contains the records to evaluate with metrics in this category. The system automatically populates this field with the same table as the metric type selected. The table does not appear in the field until you save the form.

 This field is visible depending on whether a **Type** is selected.

</td></tr><tr><td>

Weight

</td><td>

\[Required\] Numerical value that represents the importance of this category relative to other categories. A greater value indicates greater importance. For more information, see [weight categories and metrics](../concept/c_AssessmentMetrics.md). The default value is 10.

</td></tr><tr><td>

Scoring type

</td><td>

Scoring method for an attestation category. This field appears only when the [metric type](../concept/c_MetricTypesAndAssessableRecords.md) is an attestation with a **Scoring type** of **Percent**. Use this field to configure different scoring types for specific attestation categories. Possible selections are: -   **Percent**: Attestation score as a weighted percentage of correct answers for scored questions.
-   **All or nothing**: All answers for attestation type questions must be correct or the score is zero for the entire category.

</td></tr><tr><td>

Total metrics

</td><td>

\[Read-Only\] Number of metrics associated to this category.

</td></tr><tr><td>

Filter

</td><td>

Filter conditions that assessable records must meet to be evaluated using metrics in this category.

 The filter operates on fields on the selected table.

 If you specify a filter condition, the system automatically associates matching assessable records to the category when you save the record. If you change the filter conditions, the system removes and creates assessable record associations as needed. The system also deletes stakeholders for assessable records it disassociates. The system does not remove assessable record associations created by users, even if the assessable records do not match the filter conditions.

 This field is visible only when a **Type** is selected.

</td></tr><tr><td>

Description

</td><td>

Descriptive information about the category that appears on assessment questionnaires.

</td></tr><tr><td>

Roles

</td><td>

Only those users with the specified roles can perform the assessment for this category. If no role is specified, then users with any role can perform the assessment for this category.**Note:** If the **Roles** property does not appear on the form, ask your admin to add the property.

</td></tr><tr><td>

Details

</td><td>

Text field containing an HTML editor. Use this field to present important details about this category to assessment recipients. Details can include formatted lists, images, videos, or links to external websites. You may need to configure the form to see this field.

</td></tr><tr><td class="sub-head" colspan="2">

Related Lists

</td></tr><tr><td>

Assessment Metrics

</td><td>

All metrics associated to this category. There must be at least one metric associated to the category to use any assessments with the category.

</td></tr><tr><td>

Assessable records

</td><td>

All assessable records associated to this category. There must be at least one assessable record associated to the [category](../concept/c_AssessmentMetrics.md) to use any assessments with the category. This related list is hidden if the **Evaluation method** is **Attestation**. **Note:** Category users are automatically generated based on the user field is specified in the **Assessors** tab of the assessment after publishing the assessment.

</td></tr><tr><td>

Users

</td><td>

All users associated to this category. There must be at least one category user to create scheduled assessments using metrics in this category.

 If any user field is specified in the **Assessors** tab of the assessment, the corresponding users are automatically generated after publishing the assignment.

 This related list is available only when the associated metric type has schedule type set to **Scheduled**. Category users are not a part of the [on-demand assessment](../concept/c_OnDemandAssessments.md) process.

</td></tr></tbody>
</table>**Parent Topic:**[Assessments reference](assessment-reference.md)

**Related topics**  


[Create a category for assessable records](../task/t_CreateACategoryAR.md)

