---
title: View an assessment instance
description: An assessment instance represents one occurrence of a questionnaire assigned to one user.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Scheduled assessments, Assessment administrator tasks, Using assessments, Assessments, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# View an assessment instance

An assessment instance represents one occurrence of a questionnaire assigned to one user.

## Before you begin

Role required: survey\_admin, assessment\_admin, or admin

## Procedure

1.  Navigate to **All** &gt; **Assessments** &gt; **Assessment Instances**.

    The following sub-modules are available based on the state of the instances:

    -   **Ready to take**: Displays assessment instances that are ready to be taken by the user. By default, these instances are sorted in ascending order by the **Number** field.
    -   **In progress**: Displays assessment instances that are in progress. By default, these instances are sorted in ascending order by the **Number** field.
    -   **Completed**: Displays assessment instances that are complete. By default, these instances are sorted in descending order by the **Taken on** field.
    -   **Cancelled**: Displays assessment instances that are cancelled. By default, these instances are sorted in ascending order by the **Number** field.
    -   **All**: Displays assessment instances in all states. By default, these instances are sorted in ascending order by the **Number** field.
2.  Open the record from the required sub-module by clicking an assessment instance number.

    By default, the fields in the following table are displayed in the Assessment Instance form for all sub-modules other than **Completed**.

    **Note:** When you open an instance in the **Completed** sub-module, you are redirected to the User's Response page.

<table id="table_zlp_w53_dr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Auto-generated record number.

</td></tr><tr><td>

Metric type

</td><td>

Metric type of this assessment.

</td></tr><tr><td>

Assessment group

</td><td>

Assessment group to which this assessment belongs.

</td></tr><tr><td>

Due date

</td><td>

Date by which the assessment instance must be completed. The system populates the due date from the value in the metric type **Assessment duration** field. The system generates email notifications related to the due date.**Note:** By default, the system runs the Cancel Expired Assessments script every 30 days to cancel expired survey, assessment, and quiz instances that are in the Work in progress or Ready to take states.

</td></tr><tr><td>

State

</td><td>

State of the assessment.

</td></tr><tr><td>

Domain

</td><td>

Domain associated with the instance.

</td></tr><tr><td>

Assigned to

</td><td>

User this assessment is assigned to. This field becomes read-only when the state is **In progress**, **Complete**, or **Canceled**.

</td></tr><tr><td>

Signature

</td><td>

Name of the [signature record](t_CreateAnAssessmentSignature.md) attached to this assessment. A signature requires that assessment recipients acknowledge that they have read any assertions attached to a questionnaire.

</td></tr><tr><td>

Signature result

</td><td>

Verification provided by the recipient when a signature is required. This value is either the recipient's full name from the User \[sys\_user\] table or **checked**, indicating that the recipient acknowledged reading the assertion by selecting a check box.

</td></tr></tbody>
</table>3.  Click **Take assessment** to open the questionnaire.

    For more information, see [Take an assessment](t_TakeAnAssessment.md).

    This button is available if all the following conditions are true for the assessment instance:

    -   It is **Assigned to** you.
    -   The **State** is **Ready to take** or **In progress**.
    -   The associated metric type is **Active**.

**Parent Topic:**[Scheduled assessments](../concept/c_ScheduledAssessments.md)

**Related topics**  


[Assessment generation](../concept/c_AssessmentGeneration.md)

[Generate a scheduled assessment manually](t_GenSchedAssessmentManually.md)

[Event scheduling](https://www.servicenow.com/docs/access?context=c_ScheduleEvents&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)

