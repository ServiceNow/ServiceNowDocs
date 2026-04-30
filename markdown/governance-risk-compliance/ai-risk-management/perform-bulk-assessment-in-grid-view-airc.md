---
title: Perform bulk assessment in grid view
description: Perform assessments on multiple risks and controls simultaneously in a risk assessment project in the grid view using AI Risk and Compliance Workspace. You can assess inherent risks, effectiveness of controls, residual risks, and target risks. You can define risk responses that enable you to manage and mitigate the risks identified during the risk assessment process.
locale: en-US
release: yokohama
product: AI Risk Management
classification: ai-risk-management
topic_type: task
last_updated: "2025-11-27"
reading_time_minutes: 3
breadcrumb: [Use, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Perform bulk assessment in grid view

Perform assessments on multiple risks and controls simultaneously in a risk assessment project in the grid view using AI Risk and Compliance Workspace. You can assess inherent risks, effectiveness of controls, residual risks, and target risks. You can define risk responses that enable you to manage and mitigate the risks identified during the risk assessment process.

## Before you begin

Role required: sn\_risk\_advanced.risk\_asmt\_project\_reader and sn\_risk\_advanced.ara\_assessor

## About this task

You can perform the bulk risk assessment either from the Employee Center or AI Control Tower Workspace.

## Procedure

1.  To perform bulk risk assessment from the Employee Center, do the following:

    1.  Navigate to **All** &gt; **Self-Service** &gt; **Employee Center**.

    2.  On the Employee Center landing page, select **GRC Tasks**.

    3.  Select **Open** and navigate to **Bulk risk assessment**.

    4.  Open the risk assessment project that you want to assess.

2.  To perform bulk risk assessment from the AI Control Tower Workspace, do the following:

    1.  Navigate to **All** &gt; **AI Control Tower**.

    2.  Open the risk assessment project either from the Tasks list or from the AI asset record.

3.  Select **Grid view** to assess the risk assessment project.

4.  Select **Open assessment**.

    A spreadsheet-style interface appears to assess risks and controls in a grid-based view.![Grid view of risk assessment project](../image/grid-view-airc.png)

    **Note:** If more than one assessor is defined in the Stakeholder section, the assessor who opens the assessment first becomes the current assessor of the risk assessment project.

5.  To reassign the project, select the ![more actions.](../../grc-compliance-case-mgmt/image/more-actions-vertical-icon.png), and select **Reassign**.

6.  To add risks to the project, you can do the following:

    1.  To create risks from the risk statement, select the ![more actions.](../../grc-compliance-case-mgmt/image/more-actions-vertical-icon.png) icon, and select **Create from risk statements**.

    2.  To add a risk that is not in the library, select the ![more actions.](../../grc-compliance-case-mgmt/image/more-actions-vertical-icon.png) icon, and select **Create ad hoc risk**.

    3.  To add any underlying risks that have been removed, select the ![more actions.](../../grc-compliance-case-mgmt/image/more-actions-vertical-icon.png) icon, and select **Add risk**.

    The risks with an in-progress assessment can't be added as part of the risk assessment project.![Add risks in the risk assessment project](../image/grid-add-risks-airc.png)

7.  To remove risks from the project, you can do the following:

    Removed scoped risks remain part of the project but are marked as not applicable for reporting purposes. However, removed ad hoc risks are completely deleted.

    1.  Select **Actions**.

        ![Remove risks from the risk assessment project](../image/grid-remove-risks-airc.png)

    2.  Select **Remove risk**.

        Remove risk dialog box appears.

    3.  In the remove risk dialog box, provide justification and select **Remove**.

        The selected risk is deleted, along with all associated responses.

8.  Respond to all the factors in Inherent assessment for each risk within the project.

    The application automatically saves your responses and calculates the overall risk score.

9.  To assess controls, select **Yes** in the Applicable column under Control assessment, and then respond to the control effectiveness.

10. To assess residual and target assessment \(if applicable\), select **Yes** in the Applicable column.

    The application automatically calculates the final computed scores for individual assessments.

11. Select a risk response strategy and create a risk response task.

12. To view the complete summary of the assessment, select **View summary**.

13. To check for any errors in the assessment before you submit the assessment, select the ![more actions.](../../grc-compliance-case-mgmt/image/more-actions-vertical-icon.png) icon, and select **Validate**.

    You can see the list of errors, if any, that must be resolved in the side panel for the selected risk.

14. Identify the errors and resolve them.

15. Select **Validate** to check if the errors have been resolved.

16. To submit the risk assessment project for approval, select **Submit**, and select **Confirm Submission**.

    Assessments are validated again in this stage. Review the assessment summary before you submit. You can’t make any changes after submission.


**Parent Topic:**[Using AI Risk and Compliance](../concept/using-ai-risk-and-compliance.md)

