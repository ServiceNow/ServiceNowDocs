---
title: Schedule risk assessments in the Risk Workspace
description: Schedule risk assessments automatically for multiple entities. The risk assessment scheduler helps the risk managers save time by automatically initiating the assessments based on the defined frequency.
locale: en-US
release: xanadu
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2026-01-06"
reading_time_minutes: 3
breadcrumb: [Use Risk Workspace, Risk Management, Governance, Risk, and Compliance]
---

# Schedule risk assessments in the Risk Workspace

Schedule risk assessments automatically for multiple entities. The risk assessment scheduler helps the risk managers save time by automatically initiating the assessments based on the defined frequency.

## Before you begin

Role required: sn\_risk\_workspace.IT\_risk\_manager and sn\_risk\_workspace.operational\_risk\_manager

## About this task

In most organizations, the second line of risk managers is responsible for coordinating risk assessments. This group identifies the entities and associated risks that require assessment. They also determine the individuals responsible for assessing these risks. However, this continuous cycle of risk assessment demands that risk managers create individual risk assessment scopes and initiate assessments, leading to a significant loss of their time. To address this issue, the risk assessment scheduler can be used. By using the scheduler, you can schedule assessments and specify their frequency. The system initiates the assessments automatically based on the defined frequency. Additionally, you can designate the assessors and approvers for each assessment.

## Procedure

1.  Navigate to **All** &gt; **Risk** &gt; **Risk Workspace**.

2.  Select the list ![](../image/list-icon-risk-workspace.png).

3.  Navigate to **Risk assessment planning** &gt; **Scheduled assessments**.

4.  Select **New**.

    The Assessment Scheduler playbook opens the Scope definition stage, where you define the risk assessment methodology \(RAM\) and assessable entity.

    ![Assement scheduler.](../image/assessment-scheduler-playbook.png)

5.  On the Scope definition activity card, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Risk assessment methodology|Risk assessment methodology \(RAM\) that you use to assess risks.|
    |Applicable entity classes|Entity classes related to the selected RAM. The value of this field changes based on the entity classes specified in your selected RAM. This field is automatically set based on the applicable entity classes for the selected RAM.|

6.  Select **Continue**.

    The Assessable entity selection activity card opens up, enabling you to add the assessable entities that belong to the applicable entity classes.

7.  To add entities, select **Add** and do the following:

    1.  Select the entities to add.

    2.  Select **Add**.

8.  Select **Mark as complete**.

    The Assignment stage in the Assessment scheduler playbook opens.

9.  On the Assignment activity card, fill in the fields.

<table id="table_ixd_sfg_qxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assessor type

</td><td>

Individual or group who is responsible for assessing the risk. Choices are as follows:-   Entity owners
-   Risk owners
-   Group


</td></tr><tr><td>

Assessor group

</td><td>

Group that is responsible for assessing the risk. This field appears only when **Group** is selected from the **Assessor type** field.

</td></tr><tr><td>

Approver type

</td><td>

Individual or group who is responsible for approving the assessment. Choices are as follows:-   Entity owners
-   Assessor's manager
-   Group
-   None


</td></tr><tr><td>

Approver group

</td><td>

Group that is responsible for approving the assessment. This field appears only when **Group** is selected from the **Approver type** field.

</td></tr></tbody>
</table>10. Select **Mark as complete**.

    The Reassessment frequency stage in the Assessment scheduler playbook opens.

11. On the Reassessment frequency activity card, fill in the fields.

<table id="table_a4n_hhg_qxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Initiate later

</td><td>

Option to initiate the assessments on a future date.

</td></tr><tr><td>

Initiate assessments on

</td><td>

Date on which you want to schedule an assessment. This field appears only when the **Initiate later** option is selected.

</td></tr><tr><td>

Reassessment frequency

</td><td>

How often you want to assess risks. Choices are as follows:-   None
-   Weekly
-   Monthly
-   Quarterly
-   Semi-annually
-   Annually
**Note:** If you conduct an unplanned risk assessment before the next scheduled reassessment date, the subsequent assessment date is determined by the frequency established in the last assessment. For example, if your frequency is set as monthly and you conduct the initial assessment on January 1. Then, if you perform an unplanned assessment on January 15, the next assessment will still be based on the last assessment date.

</td></tr><tr><td>

Days to overdue

</td><td>

Number of days within which the assessment should be completed after it’s initiated. For example, if you define 10 in this field, the due date of the assessment will be set to 10 days after the date the assessment is initiated. The default value is 30.

</td></tr></tbody>
</table>12. Select **Mark as complete**.

    The Review and initiate stage in the Assessment scheduler playbook opens.

13. To initiate the assessments, select **Initiate assessments**.

    When you generate an assessment, the assessor or the assessor's group gets an email notification indicating that the assessment has been assigned to them.

14. To go back in the workflow and change the scope, assignment, or frequency, select **Redefine scope**.


## Result

The assessments are initiated. You can view all the scheduled assessments under **Risk assessment planning** &gt; **Scheduled assessments**.

**Parent Topic:**[Using the Risk Workspace](../concept/using-risk-workspace.md)

