---
title: Create a risk assessment scope and initiate assessments
description: Create a risk assessment scope to define and identify risks for an entity. Identify assessors and approvers for assessments, and define the frequency of assessments.
locale: en-US
release: zurich
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Perform Advanced Risk Assessment, Use, Risk Management, Governance, Risk, and Compliance]
---

# Create a risk assessment scope and initiate assessments

Create a risk assessment scope to define and identify risks for an entity. Identify assessors and approvers for assessments, and define the frequency of assessments.

## Before you begin

Role required: sn\_risk.admin

## About this task

You can initiate assessments after you create the scope. This process provides visibility and accurate reporting for the management team.

## Procedure

1.  Navigate to **All** &gt; **Advanced Risk Assessment** &gt; **Risk Assessment Scope** &gt; **Create**.

2.  On form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Risk assessment methodology|Risk assessment methodology \(RAM\) that you use to assess risks.|
    |Assessable Entity|Entities that are related to the entity classes that are selected in the **Applicable entity classes** field on the RAM. The value of this field changes based on the entity classes specified in your selected RAM. Only those entities that belong to the selected classes are displayed in this field.|
    |Owner|Owner of the entity. This field is automatically set based on the entity owner.|

3.  Right-click and save the form.

4.  To view a summary of assessments, click the Summary section.

    The Summary section has the following fields. These fields are populated only when you add risks to the assessment scope and when you initiate assessments:

    -   **No. of risk assessments closed**
    -   **No. of risks not assessed**
    -   **No. of ongoing risk assessments**
5.  Right-click to save the form.

6.  If you want to add existing risks, then do the following:

    1.  In the Risks related list, click **Add** to add existing risks.

    2.  From the Choose Risks window, select the risks that you want to add.

    3.  Click **Add Risks**.

    4.  To select control objectives that do not have a control for the entity, click **Create from library**.

    5.  From the Choose Risk Statements window, select what risk statements to apply and click **Create From Library**.

    6.  Click **Initiate Assessments** either for all the risk records or for the selected risk records.

        Ensure that the selected records are in either the Draft or Closed state.

    7.  To add new risks, click **New**, fill in the details, and click **Submit**.

        The newly added risks appear in the Risks related list.

7.  To apply the new settings, click **Settings**.

8.  On the form, fill in the fields.

<table id="table_i3c_trg_lkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assessor type

</td><td>

User or group who is responsible for assessing the risk. Choices are the following:-   **Same as risk owner**
-   **Specify users**
-   **Specify groups**
-   **Same as entity owner**


</td></tr><tr><td>

Assessor

</td><td>

User who is responsible for assessing the risk. This field appears only when **Specify users** is selected from the **Assessor type** field.

</td></tr><tr><td>

Assessor group

</td><td>

Group that is responsible for assessing the risk. This field appears only when **Specify groups** is selected from the **Assessor type** field.

</td></tr><tr><td>

Reassessment frequency

</td><td>

Frequency of assessment. Choices are the following:-   **None**
-   **Weekly**
-   **Monthly**
-   **Quarterly**
-   **Semi-annually**
-   **Annually**
 **Note:** If you need to perform an unplanned risk assessment before the next reassessment date, then the next assessment date will be based on the frequency set in the previous assessment. For example, if your frequency is set as monthly and you perform your first assessment on January1, and then you perform an unplanned assessment on January 15, then the next assessment will still be based on the previous assessment date.

</td></tr><tr><td>

Days to overdue

</td><td>

Number that is used to calculate the due date of the assessment starting from the date the assessment is initiated. For example, if the value in this field is 10, then the due date of the assessment will be 10 days after the date the assessment is initiated. The default value is 5.

</td></tr><tr><td>

Approver type

</td><td>

User or group who is responsible for approving the assessment. Choices are the following:-   **Same as entity owner**
-   **Same as assessor's manager**
-   **Specify users**
-   **Specify groups**
-   **None**


</td></tr><tr><td>

Approver

</td><td>

User who is responsible for approving the assessment. This field appears only when **Specify users** is selected from the **Approver type** field.

</td></tr><tr><td>

Approver group

</td><td>

Group that is responsible for approving the assessment. This field appears only when **Specify groups** is selected from the **Approver type** field.

</td></tr></tbody>
</table>    The settings that you select in this step apply to all the new risks that are added to this scope.

9.  To save the form, click **Submit**.

10. To generate the assessments, click **Initiate all assessments**.

    When you generate an assessment, the assessor receives an email notification stating that the assessment is assigned to the assessor or to the assessor's group.


## What to do next

If you want to cancel an assessment for risks that no longer need to be assessed, select the assessment and click **Cancel Assessments**.

**Note:** When a risk assessment is canceled, the risk assessors are notified about the cancellation and the tasks are removed from their queue.

**Parent Topic:**[Perform Advanced Risk Assessment](../concept/use-advanced-risk-assessment.md)

