---
title: Coaching field descriptions
description: Coaching field descriptions also include form related lists and actions.
locale: en-US
release: zurich
product: Coaching
classification: coaching
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Reference, Coaching, IT Service Management]
---

# Coaching field descriptions

Coaching field descriptions also include form related lists and actions.

## Coaching Opportunity form

<table id="table_u41_bmm_1fb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique \(COP\) number for the coaching opportunity.

</td></tr><tr><td>

Name

</td><td>

Unique name for the coaching opportunity.

</td></tr><tr><td>

Description

</td><td>

Description of the coaching opportunity.

</td></tr><tr><td>

Table

</td><td>

Table to use for the coaching opportunity.

</td></tr><tr><td>

Trainee

</td><td>

Field from the selected table that identifies the trainee.

</td></tr><tr><td>

Trainee group

</td><td>

Limit the trainees identified in the Trainee field to a group or groups of users.

</td></tr><tr><td>

Specify coach user

</td><td>

Check box to enable the **Coach** field.

</td></tr><tr><td>

Coach

</td><td>

Field from the selected table that identifies the coach.

</td></tr><tr><td>

Coach group

</td><td>

Group of coaches that assess and provide feedback to trainees.

</td></tr><tr><td>

Active

</td><td>

Check box to activate the coaching opportunity. Clear the check box to disable.

</td></tr><tr><td>

Trigger

</td><td>

Event that triggers a coaching opportunity for the selected table. Conditions for opportunities are generally unique events, such as when an incident is reassigned.

</td></tr></tbody>
</table><table id="table_azv_pmm_1fb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Random sample \(%\)

</td><td>

Percentage of the total assessments that get created. Use a random sample percentage to reduce the number of assessments that are created if too many events that meet the criteria for creating a coaching assessment occur.

</td></tr><tr><td>

Users who should be coached on every opportunity

</td><td>

Users that always get coached, regardless of random sample percentage.Because the specified users are exempted from the random sample percentage, a coaching assessment is always created when the assessment is triggered.

 Selected users might be new hires, for example, or others who require additional coaching.

 **Note:** Only shown if the **Random sample \(%\)** is less than 100.

</td></tr><tr><td>

Assessment duration

</td><td>

Amount of time before the assessment is set to **Closed Complete** state.

</td></tr><tr><td>

Prevent duplicate assessment

</td><td>

Check box to prevent an assessment from being created within a specified time period if one exists for that user for the same opportunity.

</td></tr><tr><td>

Within time period

</td><td>

Time period within which duplicate assessments are not created.**Note:** This field appears only when **Prevent duplicate assessment** check box is selected.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Survey taken by trainee|Survey selected for the trainee to provide additional feedback.|
|Survey taken by coach|Survey selected for the coach to provide additional feedback.|

|Field|Description|
|-----|-----------|
|Improvement KPI|Primary KPI used to measure the success of the coaching opportunity.|
|Strategic objective|Strategic objective affected by the coaching opportunity.|

<table id="table_j54_5df_yjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Snapshot fields

</td><td>

Field values to show in the coaching assessment unless an advanced script is used.

</td></tr><tr><td>

Advanced

</td><td>

Check box to use a script to determine the content for the snapshot.

</td></tr><tr><td>

Snapshot script

</td><td>

Script that defines the evaluation process applied to the selected table. Select the fields from the table for which you want to capture the values.For example, when analyzing the Incident table, use \#\{number\} to display the record number \(such as INC0010002\) for the incident record that triggered the coaching opportunity.

 **Note:** This field appears only if the **Advanced** check box is selected.

</td></tr></tbody>
</table>## Coaching Assessment form

<table id="table_rsx_bmm_1fb"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique \(CAS\) number for the coaching assessment.

</td></tr><tr><td>

Trainee

</td><td>

Trainee user that triggered the assessment in the coaching opportunity.

</td></tr><tr><td>

Record

</td><td>

Record associated with the assessment triggered in coaching opportunity.

</td></tr><tr><td>

Opportunity

</td><td>

Coaching opportunity number associated with the coaching assessment.

</td></tr><tr><td>

State

</td><td>

State of the assessment.

-   **Open**: New coaching opportunity.
-   **Work in Progress**: Trainee is being coached.
-   **Resolved**: All coaching and learnings have been provided to the trainee.

**Note:** Learnings may not have been completed by the trainee.

-   **Closed Complete**: Assessment has been resolved and closed.
-   **Closed Incomplete**: Assessment has been closed but was not completed, typically because the coaching assessment **Due date** has expired.

</td></tr><tr><td>

Coach group

</td><td>

Group of coaches to which the assessment is assigned.Default value is populated from the coaching opportunity form.

</td></tr><tr><td>

Coach

</td><td>

Coach user performing the assessment.This field is typically set by the coach before performing the assessment, but can also be set by a member of the coach group or by the coaching admin.

</td></tr><tr><td>

Due date

</td><td>

Date the assessment is due. After this time, the assessment is set to **Closed Incomplete** state.

</td></tr></tbody>
</table><table id="table_bqf_2zx_ffb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Description

</td><td>

Description of the assessment.

</td></tr><tr><td>

Work notes

</td><td>

Notes about the assessment \(journal field\).Additional notes can be added as the coach and trainee engage in further dialogue.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Snapshot|Field contents of the task, action, or behavior captured at the time the coaching opportunity was triggered.|

<table id="table_djs_lzx_ffb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assessment rating

</td><td>

Value of the performance of the trainee for reporting and trend-tracking purposes.-   Excellent
-   Good
-   Average
-   Poor
-   Unacceptable

</td></tr><tr><td>

Follow up Needed

</td><td>

Further action required, if any, to improve the performance of the trainee.-   **Recognize**: Trainee needs recognition for good performance.
-   **Needs Additional Coaching**: Trainee needs additional feedback from the coach.
-   **Needs Outside Training**: Trainee needs additional training outside the scope of the coaching assessment.
-   **Referral to Manager**: Indicates a major issue with the trainee performance.
-   **Create Virtual Coach**
-   **No Follow Up**

</td></tr><tr><td>

Summary

</td><td>

Summary of the coaching assessment.

</td></tr></tbody>
</table>## Coaching Assessment actions

<table id="table_smw_41y_ffb"><thead><tr><th>

Button

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Complete Assessment

</td><td>

Set the coaching assessment to **Closed Complete** state.

</td></tr><tr><td>

Reopen Assessment

</td><td>

Change the coaching assessment state from **Resolved** or **Closed Complete** back to **Work In Progress** for additional action.Either the coach or the trainee can reopen the coaching assessment.

</td></tr><tr><td>

Submit feedback

</td><td>

Feedback submitted by either a trainee or a coach from the survey form.

</td></tr><tr><td>

Delete

</td><td>

Deletes the coaching assessment from the Assessment Created by Opportunity list.

</td></tr></tbody>
</table>## Virtual Coaching form

<table id="table_nzj_cmm_1fb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Short Description

</td><td>

Description of the virtual coaching \(CVC\) record.

</td></tr><tr><td>

Table

</td><td>

Table source of coaching opportunity events.

</td></tr><tr><td>

Training

</td><td>

Record that contains related training content.

</td></tr><tr><td>

Active

</td><td>

Check box to activate the virtual coaching. Clear the check box to disable.

</td></tr><tr><td>

Advanced

</td><td>

Check box to use a script to determine when the automation triggers.

</td></tr><tr><td>

Conditions

</td><td>

Event that triggers a virtual coaching for the selected table. Conditions for virtual coachings are generally unique events.

</td></tr><tr><td>

Script

</td><td>

Script that defines the evaluation process applied to the selected table. Select the fields from the table to capture the values for.**Note:** Only shown if **Advanced** check box is selected.

</td></tr><tr><td>

Autofill fields

</td><td>

Fields to autofill under certain conditions.

</td></tr></tbody>
</table>## Training form

<table id="table_i1q_jby_ffb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique \(CMC\) number of the training.

</td></tr><tr><td>

Title

</td><td>

A short description for the training.

</td></tr><tr><td>

Category

</td><td>

Category of learning content, which is used for reporting.-   Customer experience
-   Best Practice Series
-   Soft-Skill Communication
-   Behavioral Coaching
-   Product Support

</td></tr><tr><td>

Content

</td><td>

Content for assigned users to learn.

</td></tr></tbody>
</table>The **Preview Message** related list shows the learning content in the context of the trainee.

**Parent Topic:**[Coaching reference](cf-coaching-reference.md)

