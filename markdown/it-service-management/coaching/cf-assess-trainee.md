---
title: Assess a trainee
description: Use a coaching assessment to review the work of a trainee and to provide training and feedback.
locale: en-US
release: australia
product: Coaching
classification: coaching
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Coaching your trainee, Training agents using Coaching with Learning, Coaching, IT Service Management]
---

# Assess a trainee

Use a coaching assessment to review the work of a trainee and to provide training and feedback.

## Before you begin

Role required: sn\_coaching.coach

## About this task

A trainee can view any field on the coaching assessment form and add comments to the to the **Work notes** field. A trainee can submit feedback for a coach using a survey when a coaching assessment is in resolved, closed complete, or closed incomplete state.

When an assessment is generated, all users in the Coach group receive a notification. Assessments are generated automatically \(as the result of a coaching opportunity\) or created manually. You can provide feedback for your trainees using a survey at any time during the coaching assessment.

You can create a coaching assessment from incidents, problems, change requests, or any other table that extends the task table. Enable the display of the **Create Coaching Assessment** button and create your assessments using that button.To enable display of the button:

-   Configure the UI actions on the record.
-   In the sn\_coaching.CoachingExtensionPoint extension point, make sure the getCreateAssessmentUITables method is implemented to return the name of the tables.

## Procedure

1.  Navigate to **All** &gt; **Coaching** &gt; **Coaching Assessment** and select a coaching assessment in the **Open** state.

    You can take a survey using the **Start Survey** button to provide feedback for the trainee at any point during the assessment. After you complete the survey, the score is calculated using the **Calculate coaching survey score** business rule and is automatically populated in the **Trainee Rating** field. The trainee rating generates an assessment rating that is populated in the **Assessment Rating** field.

    **Note:** Surveys are not available for assessments that are created manually.

2.  Fill in the fields on the Coaching Assessment form.

    1.  Verify the **Coach group**, which is obtained from the coaching opportunity, is accurate.

    2.  Set the coaching assessment **Coach** field to a coach.

    3.  In the **Due Date** field, enter the date when the assessment is due.

    The coaching assessment is set to **Closed Incomplete** state after the due date. Use system properties to set due dates to complete training. For more information, refer to [Coaching reference](../reference/cf-coaching-reference.md). You can disable automatic closure behavior by deactivating the **Close assessments after expiration** scheduled job.

3.  Fill in the fields in the **Notes** tab.

    1.  Add a **Description** to the coaching assessment.

    2.  Add **Work notes** to facilitate a dialog with the trainee.

4.  Review the **Snapshot** content in the **Snapshot** tab and add your feedback in the **Notes** field.

5.  Fill in the fields in the **Feedback** tab.

    1.  Set the **Assessment rating** based on the coaching experience.

        When you submit feedback for a trainee, the score in the **Trainee Rating** field, which is based on a scale of 1-10 is converted to a rating such as good or excellent. This rating displays in the **Assessment rating** field.

    2.  Set the **Follow up** action as part of coaching.

6.  Review the skills applicable to the trainee in the **Trainee Skillset** related list.

    See Skills Management for more information.

7.  Add [assigned training content](cf-identify-learning-content.md) in the **Assigned course items** related list.

8.  Review survey feedback for the trainee in the **Survey Results** related list.

9.  When coaching is finished:

    1.  Add a **Summary** of the coaching experience as an overview of your assessment.

    2.  Set the coaching assessment to **Resolved**.


## Coach assesses trainee

|Field|Value|
|-----|-----|
|Number|CAS0001004|
|Trainee|Trainee User 2|
|Record|Incident: INC0000055|
|Opportunity|COP0000109|
|State|Work in Progress|
|Coach group|Coach Group|
|Coach|Coach User 1|
|Due date|2018-10-25 05:18:59|

<table id="table_xgc_kb3_4fb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr class="sub-head"><td colspan="2">

Information for Review

</td></tr><tr><td>

Snapshot

</td><td>

-   Configuration item:

SAP Human Resources

-   Additional comments:

2018-06-23 21:45:04 - ITIL User \(Additional comments\)

The SAP Human Resources application is not accessible.

-   Work notes:

2018-06-23 21:45:04 - ITIL User \(Work notes\)

I cannot access this application so we may have an outage.


</td></tr><tr><td class="sub-head" colspan="2">

Feedback Rating

</td></tr><tr><td>

Assessment rating

</td><td>

Excellent

</td></tr><tr><td>

Follow up

</td><td>

Recognize

</td></tr><tr><td>

Summary

</td><td>

Trainee showed great interest in learning the trainings and finished them ahead of due date.

</td></tr></tbody>
</table>-   **[Assign skills after completing an assessment](cf-assign-skills-assessment.md)**  
Automatically assign skills to trainees for specific skill levels based on the course items they have completed. For example, if a trainee completes the course items for learning Japanese at an expert level, then the skill level 'expert' can be assigned to the trainee.

**Parent Topic:**[Coaching your trainee](../concept/cf-coaching-your-trainee.md)

**Related topics**  


[Coaching field descriptions](../reference/cf-coaching-field-descriptions.md)

