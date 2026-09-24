---
title: Assess Risk Projects in Grid view
description: Perform assessments on multiple risks and controls simultaneously in a risk assessment project using the grid view. You can assess inherent risks, effectiveness of controls, residual risks, and target risks. You can define risk responses that enable you to manage and mitigate the risks identified during the risk assessment process.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-risk-management-workspace/perform-assessment-risk-assessment-project-grid-view.html
release: brazil
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Risk assessment project, Use Risk Workspace, Risk Management, Governance, Risk, and Compliance]
---

# Assess Risk Projects in Grid view

Perform assessments on multiple risks and controls simultaneously in a risk assessment project using the grid view. You can assess inherent risks, effectiveness of controls, residual risks, and target risks. You can define risk responses that enable you to manage and mitigate the risks identified during the risk assessment process.

## Before you begin

Role required: sn\_grc.business\_user, sn\_risk\_workspace.IT\_risk\_manager, and sn\_risk\_workspace.operational\_risk\_manager

**Note:** You must manually add the sn\_risk\_advanced.risk\_asmt\_project\_reader and sn\_risk\_advanced.ara\_assessor roles to sn\_grc.business\_user to perform assessments on the risk assessment project.

## Procedure

1.  Navigate to **All** &gt; **Risk** &gt; **Risk Workspace** &gt; **My tasks**.

2.  Open the risk assessment project that you want to assess and do one of the following.

3.  Select **Grid view** to assess the risk assessment project.

    \[Omitted image "assessment-view.png"\] Alt text: Assessment view of the project

4.  Select **Open assessment**.

    A spreadsheet-style interface appears to assess risks and controls in grid based view.\[Omitted image "risk-assessment-project-grid.png"\] Alt text: Grid view of risk assessment project

5.  Review the grid.

    **Risk** and **Entity** are always shown as the first two columns. You can filter and sort risks by the **Risk** or **Entity** column. An administrator can configure additional columns to display in grid mode from the risk assessment methodology. For more information, see [Risk Assessment Methodology form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-risk-management-workspace/risk-assessment-methodology-form.md). The project header shows **Entities validated**, which tracks how many of the project's assessable entities have passed validation.

6.  To reassign the project, select the \[Omitted image "more-actions-vertical-icon.png"\] Alt text: more actions., and select **Reassign**.

7.  To add risks to the project, you can do the following:

    1.  To create risks from the risk statement, select the \[Omitted image "more-actions-vertical-icon.png"\] Alt text: more actions. icon, and select **Create from risk statements**.

    2.  To add a risk that is not in the library, select the \[Omitted image "more-actions-vertical-icon.png"\] Alt text: more actions. icon, and select **Create ad hoc risk**.

    3.  To add any underlying risks that have been removed, select the \[Omitted image "more-actions-vertical-icon.png"\] Alt text: more actions. icon, and select **Add risk**.

    The risks with an in-progress assessment can't be added as part of the risk assessment project.\[Omitted image "add-risks-more-actions.png"\] Alt text: Add risks from more actions

8.  To remove risks from the project, you can do the following:

    Removed scoped risks remain part of the project but are marked as not applicable for reporting purposes. However, removed ad hoc risks are completely deleted.Each assessable entity must have at least one scoped risk, so you can't remove the last risk that's scoped to an entity.

    1.  Select **Actions**.

        \[Omitted image "grid-remove-risks.png"\] Alt text: Remove risks in grid view.

    2.  Select **Remove risk**.

        Remove risk dialog box appears.

    3.  In the remove risk dialog box, provide justification and select **Remove**.

        The selected risk is deleted, along with all associated responses.

9.  Respond to all the factors in Inherent assessment for each risk within the project.

    The application automatically saves your responses and calculates the overall risk score.\[Omitted image "grid-control-assessment.gif"\] Alt text: Assess risks in the grid view

10. To assess controls, select **Yes** in the Applicable column under Control assessment, and then respond to the control effectiveness.

    \[Omitted image "grid-control-assessment.gif"\] Alt text: Assess controls in grid view.

11. To assess residual and target assessment, select **Yes** in the Applicable column.

    The application automatically calculates the final computed scores for individual assessments.

12. Select a risk response strategy and create a risk response task.

    \[Omitted image "grid-risk-response-task.gif"\] Alt text: Create risk response tasks in the grid view.

13. To view the complete summary of the assessment, select **View summary**.

14. To check for any errors in the assessment before you submit the assessment, select the \[Omitted image "more-actions-vertical-icon.png"\] Alt text: more actions. icon, and select **Validate**.

    You can see the list of errors, if any, that must be resolved in the side panel for the selected risk.

15. Identify the errors and resolve them.

16. Select **Validate** to check if the errors have been resolved.

17. To submit the risk assessment project for approval, select **Submit**, and select **Confirm Submission**.

    Assessments are validated again in this stage. Review the assessment summary before you submit. You can’t make any changes after submission.For a project with multiple entities, **Submit** stays disabled until all the risks across all the scoped entities pass validation.


**Parent Topic:**[Risk assessment project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-risk-management-workspace/risk-assessment-project.md)

