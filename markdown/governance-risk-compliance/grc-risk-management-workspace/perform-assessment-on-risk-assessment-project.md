---
title: Perform assessment on a risk assessment project in stacked view
description: Perform assessments on multiple risks and controls simultaneously in a risk assessment project using Risk Workspace. You can assess inherent risks, effectiveness of controls, residual risks, and target risks. You can define risk responses that enable you to manage and mitigate the risks identified during the risk assessment process.
locale: en-US
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2026-04-28"
reading_time_minutes: 2
breadcrumb: [Risk assessment project, Use Risk Workspace, Risk Management, Governance, Risk, and Compliance]
---

# Perform assessment on a risk assessment project in stacked view

Perform assessments on multiple risks and controls simultaneously in a risk assessment project using Risk Workspace. You can assess inherent risks, effectiveness of controls, residual risks, and target risks. You can define risk responses that enable you to manage and mitigate the risks identified during the risk assessment process.

## Before you begin

Role required: sn\_grc.business\_user, sn\_risk\_workspace.IT\_risk\_manager, and sn\_risk\_workspace.operational\_risk\_manager

**Note:** You must manually add the sn\_risk\_advanced.risk\_asmt\_project\_reader and sn\_risk\_advanced.ara\_assessor roles to sn\_grc.business\_user to perform assessments on the risk assessment project.

## Procedure

1.  Navigate to **All** &gt; **Risk** &gt; **Risk Workspace** &gt; **My tasks**.

2.  Open the risk assessment project that you want to assess.

3.  Select **Stacked view** to assess the risk assessment project.

4.  Select **Open assessment**.

5.  To start the assessment, select **Let's get started**.

    If you're performing reassessment, Copy risk assessments dialog box appears. Select **Yes** to copy responses from the previous risk assessment.

6.  To reassign the project, select the ![more actions.](../../grc-compliance-case-mgmt/image/more-actions-vertical-icon.png) icon, and select **Reassign**.

7.  To add risks to the project, you can do the following:

    1.  To create risks from the risk statement, select the ![more actions.](../../grc-compliance-case-mgmt/image/more-actions-vertical-icon.png) icon, and select **Create from risk statements**.

    2.  To add a risk that is not in the library, select the ![more actions.](../../grc-compliance-case-mgmt/image/more-actions-vertical-icon.png) icon, and select **Create ad hoc risk**.

    3.  To add any underlying risks that have been removed, select the ![more actions.](../../grc-compliance-case-mgmt/image/more-actions-vertical-icon.png) icon, and select **Add risk**.

    The risks with an in-progress assessment can't be added as part of the risk assessment project.

8.  To remove risks from the project, you can do the following:

    Removed scoped risks remain part of the project but are marked as not applicable for reporting purposes. However, removed ad hoc risks are completely deleted.

    1.  Select **Actions**.

    2.  Select **Remove risk**.

        Remove risk dialog box appears.

    3.  In the remove risk dialog box, provide justification and select **Remove**.

        The selected risk is deleted, along with all associated responses.

9.  Respond to all the factors in Inherent, Control, and Residual assessments, and define a risk response strategy for each risk within the project.

    The application automatically saves your responses and calculates the overall risk score.

10. To view the complete summary of the assessment, select **View summary**.

11. To check for any errors in the assessment before you submit the assessment, select the ![more actions.](../../grc-compliance-case-mgmt/image/more-actions-vertical-icon.png) icon, and select **Validate**.

    You can see the list of errors, if any, that must be resolved in the side panel for the selected risk.

12. Identify the errors and resolve them.

13. Select **Validate** to check if the errors have been resolved.

14. To submit the risk assessment project for approval, select **Submit**, and select **Confirm Submission**.

    Assessments are validated again in this stage. Review the assessment summary before you submit. You can’t make any changes after submission.


**Parent Topic:**[Risk assessment project](../concept/risk-assessment-project.md)

