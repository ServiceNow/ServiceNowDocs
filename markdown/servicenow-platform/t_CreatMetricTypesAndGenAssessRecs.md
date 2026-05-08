---
title: Create metric types and generate assessable records
description: Create a metric type, which sets a table and filter conditions that define a set of records to evaluate.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 11
breadcrumb: [Metric types and assessable records, Create an assessment metric for a category, Assessment metrics, Assessment administrator tasks, Using assessments, Assessments, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create metric types and generate assessable records

Create a metric type, which sets a table and filter conditions that define a set of records to evaluate.

## Before you begin

Role required: assessment\_admin or admin

## About this task

For example, the Vendor Performance application provides the **Vendor** metric type, which defines an assessable record for each source record in the Company \[core\_company\] table that has the **Vendor** field selected. Create a metric type for each set of records you want to evaluate, such as vendors, users within an organization, or projects.

In addition to defining assessable records, metric types also determine how to filter decision matrix data and set the schedule type, which determines whether assessments are on-demand or scheduled.

## Procedure

1.  Navigate to **All** &gt; **Assessments** &gt; **Metric Definition** &gt; **Types**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_d34_25r_jp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

\[Required\] Name of the type. It may be practical to give the type a name that indicates which records it defines.

</td></tr><tr><td>

Assessment duration

</td><td>

Amount of time assessors have to complete their assigned questionnaires, starting from the time the assessment is generated. The assessment duration sets the **Due date** that appears on [assessment instances](../concept/c_AssessmentInstances.md). Changes made to the duration of an attestation in the GRC Control Test Definition form are updated dynamically in this field. The default duration is 14 days.

</td></tr><tr><td>

Live feed

</td><td>

Check box that determines whether to enable \(selected\) or disable \(cleared\) the Live Feed view in scorecards for all assessable records created from this type.

</td></tr><tr><td>

Notify manager if overdue

</td><td>

Check box that determines whether to send \(selected\) email notifications a user's manager when that user fails to submit an assigned questionnaire on time.

</td></tr><tr><td>

Assessment manager

</td><td>

Manager for this assessment metric type. These users are responsible only for managing the assessment process and not the results. The system notifies the assessment manager when an assessment for this metric type is past due.

</td></tr><tr><td>

Scoring type

</td><td>

Scoring method to use for questions with a data type of attestation. The possible selections are:-   **Percent**: Attestation score as a weighted percentage of correct answers for scored questions. When you select this scoring type, categories can be scored as **Percent** or **All or nothing**.
-   **All or nothing**: Requires all answers for attestation type questions to be correct, or the score is zero for the entire attestation. When you select this scoring type, all categories are scored automatically as **All or nothing**.


</td></tr><tr><td>

Scale factor

</td><td>

\[Required\] Number to represent the best possible score for assessment results. All results for assessments of this type are scaled to this number. 10 is generally a good scale factor.**Note:** This field becomes read-only when it contains a value and you save the metric type. Choose a scale factor you are satisfied with before you save the metric type.

</td></tr><tr><td>

Pagination setting for Service Portal view

</td><td>

Specify how the user will see pages on the desktop or tablet view in Service Portal.-   **Category**: Display each category on a separate page. The categories appear in the following order:
    -   Each category appears in sequence on a separate page for the first assessable record
    -   Then each category appears in sequence on a separate page for the next assessable record
    -   and so on
-   **Question**: Display each question on a separate page. Questions appear on separate pages for mobile devices regardless of this setting. Each question appears for each category as described for the **Category** setting.
-   **None**: All items on a single page—no pagination
Default: **Category** **Note:** This field appears only when Service Portal is installed.

</td></tr><tr><td>

Roles

</td><td>

Additional user roles that can view the results and access records associated with this type. Users with the specified roles have read access to this type record as well as to associated categories, metrics, assessable records and scorecards, category users, stakeholders, and decision matrixes.**Note:** Users with these roles do not have access to Assessments modules unless they are also assessment administrators. Users with these roles can navigate to the records by other means, such as from reference fields on assessment instances. This field provides the option to easily grant certain users access to specific assessment data in special cases. For example, the **Vendor** metric type provides access to users with the vendor\_manager role so they can view results and compare assessable records when they open scorecards or decision matrixes in the Vendor Performance application.

</td></tr><tr><td>

Signature

</td><td>

\[Optional\] Acknowledgement by a survey recipient of requirements, admonitions, or expectations related to an assessment. For more information, see [Create an assessment signature](t_CreateAnAssessmentSignature.md).

</td></tr><tr><td>

Return URL

</td><td>

Destination address of a web page that is presented to users after they submit an assessment for this metric type. When a return URL is configured, the end note content does not appear.

</td></tr><tr><td>

State

</td><td>

\[Read-Only\] Status of the assessment: **Draft** or **Published**.

</td></tr><tr><td>

Business rule

</td><td>

\[Admin only\] Business rule the system creates to monitor the specified table. When a new record is added to the table that meets the metric type conditions, the business rule generates a corresponding assessable record.If someone changes the table or conditions of the metric type, the system updates the business rule to reflect the changes. Existing assessable records associated with the metric type are not affected.

</td></tr><tr><td>

Schedule type

</td><td>

Setting that determines which assessment process to use. Select **On demand** or **Scheduled**.

</td></tr><tr><td>

Scheduled job

</td><td>

\[Admin only\] Scheduled job the system creates to generate assessments for this metric type. This field is populated the first time you save the record. The scheduled job name follows the format &lt;type name&gt; Assessment Creation. Administrators can configure a recurring assessment generation schedule for the metric type.This field is visible only when the schedule type is **Scheduled**.

**Note:** If you change the schedule type from **Scheduled** to **On demand**, the system deletes the scheduled job. If you change the schedule type back to **Scheduled**, the system creates a new scheduled job. The previous assessment generation schedule is not saved, but can be reconfigured if desired.

</td></tr><tr><td>

Evaluation method

</td><td>

\[Admin only\] Indicates the evaluation method for this metric type. The system sets this field based on how the metric type is created. The possible evaluation methods are:-   **Assessment**: Default filter value for metric types. Only this evaluation method uses assessable records, conditions, and stakeholders.
-   **Attestation**: For details, see

Attestations - Legacy.

-   **Survey**: For details, see [Survey definitions](../../survey-administration/concept/c_SurveyDefinitions.md).


</td></tr><tr><td>

Scale factor

</td><td>

\[Required\] Number to represent the best possible score for assessment results. All results for assessments of this type are scaled to this number. **10** is generally a good scale factor. **Note:** This field becomes read-only when it contains a value and you save the metric type. Choose a scale factor that you are satisfied with before you save the metric type.

</td></tr><tr><td>

Allow retake

</td><td>

Check box that allows users to modify their answers to a completed assessment, quiz, survey, or attestation. After the due date, the system removes the assessment from the user's My Assessments and Surveys page.

</td></tr><tr><td>

Active

</td><td>

Check box that determines whether the metric type is active. When the metric type is inactive \(cleared\), assessment generation is disabled and users cannot take existing assessments.

</td></tr><tr><td>

Description

</td><td>

Helpful information about this type. Enter a clear description of the type and its purpose.

</td></tr><tr><td>

Introduction

</td><td>

Introductory content to display on assessment questionnaires. Consider adding a company logo, a welcome message, background information about the survey, or instructions. You may need to configure the form to see this field.

</td></tr><tr><td>

End note

</td><td>

Content to display on the screen that appears when someone submits an assessment questionnaire. Consider adding a thank you message, followup instructions, or other applicable information. You may need to configure the form to see this field. End notes are not displayed if a **Return URL** is specified.

</td></tr><tr><td>

Send notifications

</td><td>

Select the check box to send notifications for this assessment, survey, or attestation. You may need to configure the form to see this field.

</td></tr><tr><td colspan="2">

Condition section

</td></tr><tr><td>

Table

</td><td>

\[Required\] Table that contains the records you want to evaluate. The system creates assessable records for records on this table that meet the conditions you specify, if any. The number of matching records appears as a link by the **Condition** field. The link dynamically updates if you change the table selection. Click the link to open the list of matching records in a new tab or window.**Note:** Additional roles are required to view the records on certain tables. If you select a table that you do not have access to, a warning message appears by the **Condition** field where the number of matching records would be. You cannot generate assessable records for tables you do not have sufficient roles for.

</td></tr><tr><td>

Enforce condition

</td><td>

Check box that determines what happens to assessable records when you change the selected table or conditions.

</td></tr><tr><td>

Condition

</td><td>

Condition builder that defines specific records to assess from the selected table. If you do not specify any conditions, the system creates assessable records for all records on the selected table. Click the refresh icon to update the adjacent record count.**Note:** If you change the table or conditions, you must click **Generate Assessable Records** to create new assessable records.

</td></tr><tr><td colspan="2">

Decision Matrix section

</td></tr><tr><td>

Filter field

</td><td>

\[Required\] Field on the selected table that can be used to filter results on decision matrixes and scorecards. For example, if the selected table is **Company** `[core_company]` and you choose **Vendor type** as the filter field:-   When you view decision matrixes for this type, the decision matrix menu to filter plotted items lists vendor types: **Applications**, **Hardware**, **Services**, and **Software**.
-   On scorecards for this type, the Averages view displays ratings by vendor type.


</td></tr><tr><td>

Filter condition

</td><td>

Condition builder that defines which records from the table are available as choices on the filter menu. For example, if the filter field is **Vendor type** and you create the filter condition **\[Name\] \[does not contain\] \[Hardware\]**, only records with vendor types of **Applications**, **Services**, and **Software** are possible choices as decision matrix filters.

</td></tr><tr><td>

Default matrix filter

</td><td>

Record to use as the default filter choice on decision matrixes and scorecards. The selected **Filter field** and **Filter condition** control the available record choices. To see the records, if any, click the refresh icon next to the field. Consider the case that the filter field is **Vendor type** and you select **Applications** as the default matrix filter. The filter choice on decision matrixes for this type is set to **Applications** by default. If you change the value of the **Table** or **Filter condition** field, you must click the refresh icon to view the updated **Default matrix filter** choices. If you do not, the system selects the first available choice from the updated field choices when you save the record.

</td></tr><tr><td colspan="2">

Related Lists

</td></tr><tr><td>

Metric Categories

</td><td>

All metric categories associated with the type.

</td></tr><tr><td>

Assessable Records

</td><td>

All assessable records associated with the type. This related list is hidden in the Attestation view of this form.

</td></tr></tbody>
</table>    The **Generate Assessments** button is visible to administrators in certain cases for scheduled assessments. Do not click the button until after completing the prerequisite tasks.

4.  When you are satisfied with the type settings, click **Generate Assessable Records** to save the record and create assessable records.

    You must click **Generate Assessable Records** to create the initial set of assessable records based on the table and conditions specified on the type record. After that, the system creates an assessable record each time a new matching record is created. **Generate Assessable Records** is located under **Related Links**.

    **Note:** Clicking **Generate Assessable Records** can trigger the deletion of existing assessable records under certain circumstances.For more information, see [Enforce a condition to delete an assessable record](t_EnforceACondition.md).

    The page redirects to the list of assessable records created.


**Parent Topic:**[Metric types and assessable records](../concept/c_MetricTypesAndAssessableRecords.md)

**Related topics**  


[Assessment scorecard averages](../reference/r_Averages.md)

[Schedule an assessment](t_ScheduledAssessment.md)

[Schedule types](../concept/c_ScheduleTypes.md)

[Set an assessment generation schedule](t_SetAssesstGenerationSchedule.md)

[On-demand assessments](../concept/c_OnDemandAssessments.md)

[Enforce a condition to delete an assessable record](t_EnforceACondition.md)

[Metric types and assessable records](../concept/c_MetricTypesAndAssessableRecords.md)

[bundle-platadm.configure-form-layout]

