---
title: Create a risk assessment scope in the Risk Workspace
description: Create a risk assessment scope to identify risks for an entity, define assessors and approvers, set assessment frequency, and initiate assessments using the Risk Management application.
locale: en-US
release: xanadu
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Use Risk Workspace, Risk Management, Governance, Risk, and Compliance]
---

# Create a risk assessment scope in the Risk Workspace

Create a risk assessment scope to identify risks for an entity, define assessors and approvers, set assessment frequency, and initiate assessments using the Risk Management application.

## Before you begin

Role required: sn\_risk\_workspace.IT\_risk\_manager, sn\_risk\_workspace.operational\_risk\_manager, or sn\_risk\_workspace.business\_op\_risk\_manager

## About this task

Creating a risk assessment scope ensures that assessments are effectively carried out, resulting in valuable insights for the risk management team and enabling informed decision-making. You can create a risk assessment scope with a guided experience using the playbook. Each stage within the playbook includes one or more activities that must be completed, providing a structured approach to the risk assessment scope. The playbook guides you through each stage, recommending necessary activities, and ensuring comprehensive coverage of the workflow. Stages can also include automated activities, such as auto-sending an email to the Assessor when you initiate an assessment.

## Procedure

1.  Navigate to **All** &gt; **Risk** &gt; **Risk Workspace**.

2.  Select the list ![List icon.](../../grc-workspace-audit/image/ListsIcon.jpg) icon.

3.  From the list, navigate to **Risk assessment planning** select **Scoped entities**.

4.  Select **New**.

    The Risk assessment scope playbook opens and initiates the first activity for defining the risk assessment methodology \(RAM\) and assessable entity, which is the Scope definition stage.

5.  On the Scope definition activity card, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Risk assessment methodology|Risk assessment methodology \(RAM\) that you use to assess risks.|
    |Assessable entity|Entities associated with the selected entity classes defined in the **Applicable entity classes** field on the RAM. The value of this field changes based on the entity classes specified in your selected RAM. Only those entities that belong to the selected classes are displayed in this field.|
    |Owner|Owner of the entity. This field is automatically set based on the assessable entity.|

6.  Select **Continue**.

    The Risks selection activity card opens that enables you to select and assess the risks related with the entity using the selected RAM.

7.  To add existing risks, select **Add** and do the following:

    1.  Select the risks to add.

    2.  Select **Add**.

8.  To create risks, select **Create risk** and do the following:

    1.  Fill in the details of the new risk.

    2.  Select **Save**.

9.  To create risks from the risk taxonomy, select the down arrow icon next to the **Create risk** button, select **Create from risk statements**, and do the following:

    1.  Select the risk statements to add.

    2.  Select **Add**.

10. Select **Mark as complete**.

    The Assignment stage in the Risk assessment scope playbook opens.

11. On the Assignment activity card, fill in the fields.

<table id="table_ixd_sfg_qxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assessor type

</td><td>

User or group who is responsible for assessing the risk. Choices are as follows:-   **Same as entity owner**
-   **Same as risk owner**
-   **Specify users**
-   **Specify groups**


</td></tr><tr><td>

Assessor

</td><td>

User who is responsible for assessing the risk. This field appears only when **Specify users** is selected from the **Assessor type** field.

</td></tr><tr><td>

Assessor group

</td><td>

Group that is responsible for assessing the risk. This field appears only when **Specify groups** is selected from the **Assessor type** field.

</td></tr><tr><td>

Approver type

</td><td>

User or group who is responsible for approving the assessment. Choices are as follows:-   Same as entity owner
-   Same as assessor's manager
-   Specify users
-   Specify groups
-   None


</td></tr><tr><td>

Approver

</td><td>

User who is responsible for approving the assessment. This field appears only when **Specify users** is selected from the **Approver type** field.

</td></tr><tr><td>

Approver group

</td><td>

Group that is responsible for approving the assessment. This field appears only when **Specify groups** is selected from the **Approver type** field.

</td></tr></tbody>
</table>12. Select **Mark as complete**.

    The Reassessment frequency stage in the Risk assessment scope playbook opens.

13. On the Reassessment frequency activity card, fill in the fields.

<table id="table_a4n_hhg_qxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

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

Number of days within which the assessment should be completed after it is initiated. For example, if you define a value of 10 in this field, the due date of the assessment will be set to 10 days after the date the assessment is initiated. The default value is 5.

</td></tr></tbody>
</table>14. Select **Mark as complete**.

    The Initiate assessments stage in the Risk assessment scope playbook opens.

15. To initiate the assessments, select **Initiate all assessments**.

    When you generate an assessment, the assessor or the assessor's group gets an email notification indicating that the assessment has been assigned to them.

16. To go back in the workflow and change the scope, assignment, or frequency, select the menu ![Menu icon.](../../../common/image/icon-menu.png) icon, and then select **Redefine scope**.


**Parent Topic:**[Using the Risk Workspace](../concept/using-risk-workspace.md)

