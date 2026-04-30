---
title: Assess the quality of your agent's completed tasks
description: Assess the ability of your agents to resolve incidents or the quality of their completed tasks.
locale: en-US
release: yokohama
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Surveys in Workforce Optimization for ITSM, Training your teams using Coaching in Workforce Optimization for ITSM, Coaching in Workforce Optimization for ITSM, Workforce Optimization for ITSM, IT Service Management]
---

# Assess the quality of your agent's completed tasks

Assess the ability of your agents to resolve incidents or the quality of their completed tasks.

## Before you begin

You can create an assessment from an interaction or any task type. When you manually create an assessment, you can add a survey to it. Coaching assessments also get created and assigned to the coach based on the trigger conditions that are defined in coaching opportunities.

Role required: sn\_coaching.coach

## About this task

If the [coaching opportunity](../../coaching/task/create-coaching-opportunity.md) includes a survey, you can opt to take the survey and the assessment. When you use a survey to [assess a trainee](../../coaching/task/assess-trainee.md), the score for the survey is automatically calculated when you complete the survey. The assessment rating is then updated based on that score.

The Coaching Overview screen displays the average quality of the tasks that were completed in the past 30 days for your assignment groups.

-   The donut chart displays the number of assessments in various states of completion. You can point to one of the states and click to open all assessments in that state.
-   The bar chart displays assessments created by coaching opportunities. You can click on any of the data in the graph to access the assessments.
-   You can click on the graph that displays the indicator data and access detailed information on the indicator.

## Procedure

1.  Navigate to **All** &gt; **Workforce Optimization for ITSM** &gt; **Manager Workspace**.

2.  Perform adhoc assessments or the ones triggered by coaching opportunities.

<table id="choicetable_k5z_rpq_pnb"><thead><tr><th align="left" id="d311527e109">

To

</th><th align="left" id="d311527e112">

Do this

</th></tr></thead><tbody><tr><td id="d311527e118">

**Perform adhoc assessments**

</td><td>

1.  Click the List icon.
2.  Select any record, such as an incident or change request, for which you want to create an assessment.
3.  Select the Assessments icon ![Coaching assessment icon](../image/coaching-assessment-icon.png). The assessment screen appears in the right panel.
4.  Click the plus \(+\) icon.


</td></tr><tr><td id="d311527e148">

**Use assessments triggered by coaching opportunities**

</td><td>

1.  Click the Coaching icon.
2.  Select any record for which you want to create an assessment.

**Note:** Click the **Active Assessments** tab to view assessments of all teams for which you are a manager or an additional manager.

3.  Select an incident to assess.


</td></tr></tbody>
</table>3.  On the form, fill in the fields to assess the agent.

<table id="table_j31_ys1_mlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Opportunity

</td><td>

Coaching opportunity that is associated with the coaching assessment.

</td></tr><tr><td>

State

</td><td>

State of the assessment.-   **Open**: New coaching opportunity.
-   **Work in progress**: Trainee is being coached.
-   **Resolved**: Trainee is assigned coaching programs and training modules.
-   **Closed Complete**: Assessment has been resolved and closed.
-   **Closed Incomplete**: Assessment that has been closed but not completed, typically because the coaching assessment **Due Date** has expired.


</td></tr><tr><td>

Assessment Rating

</td><td>

How well the agent resolved the incident. The Coaching application automatically populates this field when a coach completes a survey for the trainee.

</td></tr><tr><td>

Follow up

</td><td>

Whether the coach must take further action to improve the trainee performance.

</td></tr><tr><td>

Comments

</td><td>

Notes, if any, to add about the assessment.

</td></tr><tr><td>

Survey taken by coach

</td><td>

Survey for the trainee taken by the coach. You can add a survey for an assessment when you create the assessment manually or when the coaching opportunity triggers an assessment that does not have a survey.

 When a coaching opportunity triggers an assessment and contains a survey, the survey is automatically added to the assessment and cannot be changed by the coach.

</td></tr><tr><td>

Survey taken by trainee

</td><td>

Survey for the coach taken by the trainee.

</td></tr><tr><td>

Add skills

</td><td>

Skills to add to the trainee profile when the assessment is complete. When you click this field, it displays all skills and the skill levels that are not in the trainee profile.

</td></tr><tr><td>

Add training

</td><td>

Training to assign to the trainee.You can also assign learning tasks from course items.

</td></tr></tbody>
</table>4.  Do the following:

    -   To complete the adhoc assessment, click **Save**.
    -   To complete assessments creating using coaching opportunities, click **Complete assessment**.

**Parent Topic:**[Surveys in Workforce Optimization for ITSM](../concept/surveys-wfo-itsm.md)

