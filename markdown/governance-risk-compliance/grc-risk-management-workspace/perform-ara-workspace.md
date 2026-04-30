---
title: Perform advanced risk assessment in the Risk Workspace
description: Conduct risk assessments to assess inherent risks, effectiveness of controls, residual risks, and target risks in the Risk Workspace application. You can define risk responses that enable you to manage and mitigate the risks identified during the risk assessment process.
locale: en-US
release: zurich
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Use Risk Workspace, Risk Management, Governance, Risk, and Compliance]
---

# Perform advanced risk assessment in the Risk Workspace

Conduct risk assessments to assess inherent risks, effectiveness of controls, residual risks, and target risks in the Risk Workspace application. You can define risk responses that enable you to manage and mitigate the risks identified during the risk assessment process.

## Before you begin

Role required: sn\_grc.business\_user

**Note:** You must manually assign the advanced risk assessment roles to the sn\_grc.business\_user role. To understand how you can adjust the granting of roles and groups, see the [How to adjust granting of roles and groups to use background jobs \[KB0963693\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0963693) article in the Now Support Knowledge Base. You must log in to Now Support to view the article.

## About this task

A risk assessment is performed for the following:

-   Inherent risks
-   Effectiveness of controls
-   Residual risks
-   Target risks

The risk assessments yield risk scores that are automatically calculated based on the configurations made in the risk assessment methodology \(RAM\). If you want to change the automatically calculated scores, you can overwrite the calculated scores and provide a justification. If you have no controls to assess, then the residual risk score is the same as the inherent risk score.

After performing the assessment, you can define the risk response. Risk response refers to the process of managing identified risks. It’s a planning and decision-making process where the risk managers decide how to deal with each risk. While performing the assessment, you can view detailed reference information on the Contextual side panel. This panel provides information for the risk events, open issues, key indicator breaches, control test results, and control indicator failures.

If the risk assessment in being performed by an assessor's delegate, the **Assessor's delegates** field shows the delegate's name.

A risk assessment record progresses through the following statuses:

-   **New**: The risk assessment is created but not yet initiated or is in a ready-to-assess state.
-   **In progress**: The risk assessment is currently being evaluated. This status applies when the assessment is in any of the following states: Inherent Assessment, Control Assessment, Residual Assessment, Target Assessment, or Respond.
-   **Awaiting approval**: The risk assessment is complete and awaiting review or approval from the designated approvers.
-   **Completed**: The risk assessment has been fully approved, finalized, and requires no further actions.
-   **Archived**: The risk assessment is no longer active. When an assessment is in the Completed status and a reassessment begins for the same risk, the old assessment is moved to the Archived status.
-   **Cancelled**: The risk assessment has been terminated or withdrawn.

For more information on statuses, see [Risk Assessment workflow changes from 19.1.x version](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1719433) article in the Now Support Knowledge Base. You must log in to Now Support to view the article.

## Procedure

1.  Navigate to **All** &gt; **Risk** &gt; **Risk Workspace** &gt; **My tasks**.

2.  Open the risk assessment that you want to assess and do one of the following.

    -   If you want to start the assessment, select **Let's get started**.
    -   If you think that the risk assessment must be assigned to someone else, select **Reassign** and fill in the necessary details.
    -   If this risk was previously assessed, to view the previous assessment, select **Review last assessment**.
    -   If the risk assessment is in progress and you want to continue the assessment, select **Resume**.
3.  To perform inherent assessment, respond to the all inherent assessment questions.

    1.  To view the guidance for a factor, select the question mark icon \(![Show guidance for a factor.](../image/show-guidance.jpg).

    2.  To view the qualitative and quantitative weightage, select overall rating icon.

    The application automatically saves your responses and calculates the overall risk score.

4.  To change the computed inherent risk results, do the following:

    1.  Select the **I would like to change the computed score** option.

    2.  From the **Override inherent risk** field, select the appropriate value.

    3.  Enter comments that explain the reasons for the change in the computed score.

5.  Select **Next**.

6.  For the Control assessment, do one of the following:

    -   To assess the effectiveness of the controls, respond to all the control assessment factors.
    -   To proceed without assessing the mitigating controls, select the **Control assessment not applicable** option.
    -   To assess the control environment without adding controls, select **I would like to change the computed score** option and refer to step 8.
    You can also change the computed control effectiveness results by providing a justification for changing the score.

7.  To add or create controls for the control assessment, do one of the following:

    -   To add existing controls, select **Add**.
    -   To inherit common controls, select **Inherit common controls**.
    -   To create a control, select the down-arrow next to the **Inherit common controls** button, and select **Create control**.
    -   To add controls from control taxonomy, select the down-arrow next to the **Inherit common controls** button, and select **Create from control objectives**.
8.  To assess the control environment without adding controls, do the following:

    1.  Select the **I would like to change the computed score** option.

    2.  From the **Override control effectiveness** field, select the appropriate value.

    3.  Enter comments that explain the reasons for the change in the computed score.

9.  To assess the leftover risks after the implementation of mitigating controls, select **Next** and respond to the factors in the residual assessment.

    You can also change the computed residual score by providing a justification for changing the score.

10. **Note:** The availability of the target risk assessment on the assessment form depends on the conditions outlined in the RAM.

    To assess the desired risk level that you want to achieve in the future, select **Next** and respond to the factors in the target assessment.

    You can also change the computed target score by providing a justification for changing the score.

11. To select an appropriate strategy and to define the plan of action for the risks assessed, select **Next**, and do the following.

    1.  Select the appropriate risk responses.

    2.  To create a risk response task, select the **Create task** button, and select the appropriate values.

        For more information, see [Create a risk response task in the Risk Workspace](../../grc-risk/task/create-risk-response-task-risk-workspace.md).

    3.  To link existing risk response tasks or copy the tasks along with the risk response strategies from the previous assessment while reassessing a risk, select **Yes, continue with existing**.

        The **Yes, continue with existing** button appears only when you are reassessing a risk. To continue with another response, select **Change response**.

    4.  Select **Save task** and review your responses.

        The risk response tasks are created and assigned to the assignee. You can edit the task and modify it to change the owner.

12. To link existing issues to the risk assessment, do the following:

    You must enable the **Allow issue linking with risk assessment** option on the Risk Assessment Methodology \(RAM\) form to use this feature.

    1.  Select **Add existing issues**.

    2.  Select the issues from the list and select **Add**.

13. To create issues for the risk assessment, do the following:

    You must enable the **Allow issue linking with risk assessment** option on the Risk Assessment Methodology \(RAM\) form to use this feature.

    1.  Select **Create issue**.

    2.  On the Create an issue form, fill in the required details.

    3.  Select **Save**.

14. Select **Submit**.

    If there are no validation errors, the assessment homepage is displayed.

15. If you want to modify the assessment, select **Edit**.

16. To view the activities taking place for the assessment, select the Activity log icon ![Activity log icon.](../image/activity-log.jpg).

17. If you have defined approvers, then select **Submit**.

    The assessment home page is displayed. You can review the summary of your assessment.

18. To request approval, edit assignment, or reassign, select one of the following.

    |Choice|Description|
    |------|-----------|
    |**Request approval**|If an approver is specified, select this option to send the assessment for approval. You can also provide additional comments for the approver.|
    |**Edit assessment**|If you want to modify your responses in the assessment, select this option.|
    |**Reassign**|If the assessment must be assigned to someone else, select this option.|


## Result

The assessment is sent to the approver and the approval workflow starts.

## Example

![Send risk assessment for approval.](../image/risk-assessment-approval.png "In progress risk assessment ready for approval")

**Parent Topic:**[Using the Risk Workspace](../concept/using-risk-workspace.md)

