---
title: Assessment Metric form
description: Description of the field values for the Assessment Metric form.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Assessments reference, Assessments, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Assessment Metric form

Description of the field values for the Assessment Metric form.

<table id="table_xqn_x51_12b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the assessment.

</td></tr><tr><td>

Assessment duration

</td><td>

Allowed duration to complete an assignment after its generation.

</td></tr><tr><td>

Live feed

</td><td>

Checkbox that automatically creates Live Feed groups for newly generated assessable records of this type.

</td></tr><tr><td>

Notify manager if overdue

</td><td>

Checkbox to send a notification to the manager when the assessment becomes overdue.

</td></tr><tr><td>

Scale factor

</td><td>

Scale value for all assessment results.

</td></tr><tr><td>

Pagination setting for Service Portal view

</td><td>

The setting on which the pagination is based for desktop or tablet view in Service Portal.-   Category: default
-   Question: 1 question per page \(automatic for mobile\)
-   None: no pagination

 **Note:** This field is displayed only when Service Portal is installed.

</td></tr><tr><td>

Business rule

</td><td>

Business rule that is automatically created for assessable record generation.

</td></tr><tr><td>

Schedule type

</td><td>

Scheduled or on-demand assessment type.

</td></tr><tr><td>

Scheduled job

</td><td>

Scheduled job the system creates for this assessment definition when the schedule period is a repeating interval. The system sets the scheduled job to run according to the selected schedule period.-   If you change the schedule period and save the survey definition, the system deletes the old scheduled job.
-   If you selected a recurring schedule period, a new scheduled job is created.

 For example, if you change the schedule period from **Daily** to **Weekly** and save the record:

-   The system deletes the daily scheduled job.
-   Creates a weekly one set to run a week from the current date.

 This field is visible to administrators only if the schedule period is **Daily**, **Weekly**, **Monthly**, or **Yearly**.

</td></tr><tr><td>

Evaluation method

</td><td>

Type of assessment.

</td></tr><tr><td>

Roles

</td><td>

Roles with read access for this metric type.

</td></tr><tr><td>

Active

</td><td>

Check box to enable the distribution of this assessment to recipients.

</td></tr><tr><td>

Owners

</td><td>

Owners of the assessment. You can add a user with the survey\_creator, survey\_admin, or assessment\_admin role.

</td></tr><tr><td>

Description

</td><td>

Description of the assessment.

</td></tr><tr><td class="sub-head" colspan="2">

Conditions

</td></tr><tr><td>

Table

</td><td>

Table that contains records to assess for this type.

</td></tr><tr><td>

Enforce condition

</td><td>

Checkbox to delete the existing assessable records of this type that do not meet the specified conditions.

</td></tr><tr><td>

Condition

</td><td>

Conditions that the assessable records of this type should meet.

</td></tr><tr><td class="sub-head" colspan="2">

Decision Matrix

</td></tr><tr><td>

Filter field

</td><td>

Field on the Filter table to identify filter menu choices on decision matrices and scorecard averages for this type.

</td></tr><tr><td>

Filter condition

</td><td>

Conditions to filter results on decision matrices and scorecard averages for this type.

</td></tr><tr><td>

Default matrix filter

</td><td>

Default filter menu choice on decision matrix of this type.

</td></tr><tr><td class="sub-head" colspan="2">

Assessors

</td></tr><tr><td>

User field

</td><td>

User field from the table specified in the **Conditions** tab. The assessment will be assigned to all users of this user field in the table.When you save the assessment and click **Generate Assessable Records**, an assessable record is created for each unique user of the user field. This is applicable for Scheduled and On-demand assessments.

 For an on-demand assessment, each assessor assesses all assessable records. For a scheduled assessment, each assessor assesses only the corresponding assessable record.

</td></tr><tr><td class="sub-head" colspan="2">

Related Links

</td></tr><tr><td>

Generate Assessable Records

</td><td>

Creates assessable records for this metric type.

</td></tr><tr><td>

Show Benchmarks

</td><td>

Opens the Benchmarks Dashboard that provides visibility into your key performance indicators \(KPIs\) and trends.**Note:**

-   This related link is available only for survey\_admin, assessment\_admin and survey\_reader with bm\_viewer role.
-   You must opt in to Benchmarks to view the dashboard. See [Enable Benchmarks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/benchmarks/t_EnableBench.md)
-   This is applicable only for a published survey.

</td></tr><tr><td>

Create Improvement Initiative

</td><td>

Opens the Improvement Initiative window to create an improvement initiative record that helps in improving the performance of the assessment.**Note:**

-   This related link is available only for the survey\_admin and assessment\_admin role. A survey\_reader can only view the created improvement initiative records.
-   You should activate the Continual Improvement Management plugin \(com.sn\_cim\).

</td></tr><tr><td class="sub-head" colspan="2">

Related Lists

</td></tr><tr><td>

Metric Categories

</td><td>

All metric categories for this assessment.

</td></tr><tr><td>

Assessable Records

</td><td>

All assessable records for this assessment.

</td></tr><tr><td>

Improvement Initiatives

</td><td>

Displays improvement initiatives associated with the survey.**Note:** This related list is available only when there is at least one improvement initiative record.

</td></tr></tbody>
</table>**Parent Topic:**[Assessments reference](assessment-reference.md)

**Related topics**  


[Configure an assessment](../task/configure-assessment.md)

