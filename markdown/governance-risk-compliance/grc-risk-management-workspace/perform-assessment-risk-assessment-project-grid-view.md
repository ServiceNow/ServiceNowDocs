---
title: Perform assessment on a risk assessment project in grid view
description: Perform assessments on multiple risks and controls simultaneously in a risk assessment project using the grid view. You can assess inherent risks, effectiveness of controls, residual risks, and target risks. You can define risk responses that enable you to manage and mitigate the risks identified during the risk assessment process.
locale: en-US
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Risk assessment project, Use Risk Workspace, Risk Management, Governance, Risk, and Compliance]
---

# Perform assessment on a risk assessment project in grid view

Perform assessments on multiple risks and controls simultaneously in a risk assessment project using the grid view. You can assess inherent risks, effectiveness of controls, residual risks, and target risks. You can define risk responses that enable you to manage and mitigate the risks identified during the risk assessment process.

## Before you begin

Role required: sn\_grc.business\_user, sn\_risk\_workspace.IT\_risk\_manager, and sn\_risk\_workspace.operational\_risk\_manager

**Note:** You must manually add the sn\_risk\_advanced.risk\_asmt\_project\_reader and sn\_risk\_advanced.ara\_assessor roles to sn\_grc.business\_user to perform assessments on the risk assessment project.

## Procedure

1.  Navigate to **All** &gt; **Risk** &gt; **Risk Workspace** &gt; **My tasks**.

2.  Open the risk assessment project that you want to assess and do one of the following.

3.  Select **Grid view** to assess the risk assessment project.

    ![Assessment view of the project](../image/assessment-view.png)

4.  Select **Open assessment**.

    A spreadsheet-style interface appears to assess risks and controls in grid based view.![Grid view of risk assessment project](../image/risk-assessment-project-grid.png)

5.  To reassign the project, select the ![more actions.](../../grc-compliance-case-mgmt/image/more-actions-vertical-icon.png), and select **Reassign**.

6.  To add risks to the project, you can do the following:

    1.  To create risks from the risk statement, select the ![more actions.](../../grc-compliance-case-mgmt/image/more-actions-vertical-icon.png) icon, and select **Create from risk statements**.

    2.  To add a risk that is not in the library, select the ![more actions.](../../grc-compliance-case-mgmt/image/more-actions-vertical-icon.png) icon, and select **Create ad hoc risk**.

    3.  To add any underlying risks that have been removed, select the ![more actions.](../../grc-compliance-case-mgmt/image/more-actions-vertical-icon.png) icon, and select **Add risk**.

    The risks with an in-progress assessment can't be added as part of the risk assessment project.![Add risks from more actions](../image/add-risks-more-actions.png)

7.  To remove risks from the project, you can do the following:

    Removed scoped risks remain part of the project but are marked as not applicable for reporting purposes. However, removed ad hoc risks are completely deleted.

    1.  Select **Actions**.

        ![Remove risks in grid view.](../image/grid-remove-risks.png)

    2.  Select **Remove risk**.

        Remove risk dialog box appears.

    3.  In the remove risk dialog box, provide justification and select **Remove**.

        The selected risk is deleted, along with all associated responses.

8.  Respond to all the factors in Inherent assessment for each risk within the project.

    The application automatically saves your responses and calculates the overall risk score.![Assess risks in the grid view](../image/grid-control-assessment.gif)

9.  To assess controls, select **Yes** in the Applicable column under Control assessment, and then respond to the control effectiveness.

    ![Assess controls in grid view.](../image/grid-control-assessment.gif)

10. To assess residual and target assessment, select **Yes** in the Applicable column.

    The application automatically calculates the final computed scores for individual assessments.

11. Select a risk response strategy and create a risk response task.

    ![Create risk response tasks in the grid view.](../image/grid-risk-response-task.gif)

12. To view the complete summary of the assessment, select **View summary**.

13. To check for any errors in the assessment before you submit the assessment, select the ![more actions.](../../grc-compliance-case-mgmt/image/more-actions-vertical-icon.png) icon, and select **Validate**.

    You can see the list of errors, if any, that must be resolved in the side panel for the selected risk.

14. Identify the errors and resolve them.

15. Select **Validate** to check if the errors have been resolved.

16. To submit the risk assessment project for approval, select **Submit**, and select **Confirm Submission**.

    Assessments are validated again in this stage. Review the assessment summary before you submit. You can’t make any changes after submission.


**Parent Topic:**[Risk assessment project](../concept/risk-assessment-project.md)

