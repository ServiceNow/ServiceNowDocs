---
title: Perform bulk assessment in stacked view
description: Perform assessments on multiple risks and controls simultaneously in a risk assessment project using AI Risk and Compliance Workspace. You can assess inherent risks, effectiveness of controls, residual risks, and target risks. You can define risk responses that enable you to manage and mitigate the risks identified during the risk assessment process.
locale: en-US
release: zurich
product: AI Risk Management
classification: ai-risk-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Perform bulk assessment in stacked view

Perform assessments on multiple risks and controls simultaneously in a risk assessment project using AI Risk and Compliance Workspace. You can assess inherent risks, effectiveness of controls, residual risks, and target risks. You can define risk responses that enable you to manage and mitigate the risks identified during the risk assessment process.

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

3.  Select **Stacked view** to assess the risk assessment project.

4.  Select **Open assessment**.

    If more than one assessor is defined in the Stakeholder section, the assessor who opens the assessment first becomes the current assessor of the risk assessment project.

5.  To reassign the project, select the more actions icon ![](../../grc-compliance-case-mgmt/image/more-actions-vertical-icon.png), and select **Reassign**.

6.  To add risks to the project, you can do the following:

    1.  To create risks from the risk statement, select the more actions icon ![](../../grc-compliance-case-mgmt/image/more-actions-vertical-icon.png), and select **Create from risk statements**.

    2.  To add a risk that is not in the library, select the more actions icon ![](../../grc-compliance-case-mgmt/image/more-actions-vertical-icon.png), and select **Create ad hoc risk**.

    3.  To add any underlying risks that have been removed, select the more actions icon ![](../../grc-compliance-case-mgmt/image/more-actions-vertical-icon.png), and select **Add risk**.

    The risks with an in-progress assessment can't be added as part of the risk assessment project.

7.  To remove risks from the project, you can do the following:

    Removed scoped risks remain part of the project but are marked as not applicable for reporting purposes. However, removed ad hoc risks are completely deleted.

    1.  Select **Actions**.

    2.  Select **Remove risk**.

        Remove risk dialog box appears.

    3.  In the Remove risk dialog box, provide justification and select **Remove**.

        The selected risk is deleted, along with all associated responses.

8.  Respond to all the factors in Inherent, Control, and Residual assessments, and define a risk response strategy for each risk within the project.

    ![Stacked view of risk assessment project.](../image/stacked-view-airc.png)

    **Note:** The application automatically saves your responses and calculates the overall risk score.

9.  To view the complete summary of the assessment, select **View summary**.

10. To check for any errors in the assessment before you submit the assessment, select the more actions icon ![](../../grc-compliance-case-mgmt/image/more-actions-vertical-icon.png), and select **Validate**.

    You can see the list of errors, if any, that must be resolved in the side panel for the selected risk.

11. Identify the errors and resolve them.

12. Select **Validate** to check if the errors have been resolved.

13. To submit the risk assessment project for approval, select **Submit**, and select **Confirm Submission**.

    Assessments are validated again in this stage. Review the assessment summary before you submit. You can’t make any changes after submission.


**Parent Topic:**[Using AI Risk and Compliance](../concept/using-ai-risk-and-compliance.md)

