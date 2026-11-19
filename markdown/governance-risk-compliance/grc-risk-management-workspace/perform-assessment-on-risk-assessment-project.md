---
title: Assess Risk Projects in Stacked View
description: Perform assessments on multiple risks and controls simultaneously in a risk assessment project using Risk Workspace. You can assess inherent risks, effectiveness of controls, residual risks, and target risks. You can define risk responses that enable you to manage and mitigate the risks identified during the risk assessment process.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-risk-management-workspace/perform-assessment-on-risk-assessment-project.html
release: brazil
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Risk assessment project, Use Risk Workspace, Risk Management, Governance, Risk, and Compliance]
---

# Assess Risk Projects in Stacked View

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

6.  If the project has more than one assessable entity, select the **Entity** dropdown, and select the entity whose risks you want to assess.

    A validation icon next to each entity in the dropdown shows whether that entity's risks have passed validation. The list of risks updates to show only the risks that are scoped to the selected entity.

7.  To reassign the project, select the \[Omitted image "more-actions-vertical-icon.png"\] Alt text: more actions., and select **Reassign**.

8.  To add risks to the project, you can do the following:

    1.  To create risks from the risk statement, select the \[Omitted image "more-actions-vertical-icon.png"\] Alt text: more actions. icon, and select **Create from risk statements**.

    2.  To add a risk that is not in the library, select the \[Omitted image "more-actions-vertical-icon.png"\] Alt text: more actions. icon, and select **Create ad-hoc risk**.

    3.  To add any underlying risks that have been removed, select the \[Omitted image "more-actions-vertical-icon.png"\] Alt text: more actions. icon, and select **Add risk**.

    The risks with an in-progress assessment can't be added as part of the risk assessment project.

9.  To remove risks from the project, you can do the following:

    Removed scoped risks remain part of the project but are marked as not applicable for reporting purposes. However, removed ad-hoc risks are completely deleted.Each assessable entity must have at least one scoped risk, so you can't remove the last risk that's scoped to an entity.

    1.  Select **Actions**.

    2.  Select **Remove risk**.

        Remove risk dialog box appears.

    3.  In the remove risk dialog box, provide justification and select **Remove**.

        The selected risk is deleted, along with all associated responses.

10. Respond to all the factors in Inherent, Control, and Residual assessments, and define a risk response strategy for each risk within the project.

    The application automatically saves your responses and calculates the overall risk score. The response options are Accept, Avoid, Mitigate and Transfer, shown as checkboxes, with a rationale box. In the Residual assessment, select **Residual assessment not applicable** if it doesn't apply. Only mandatory factors block submission. The Control assessment is pre-completed from automated factors, so you don't answer it.

11. To create a risk response task for a strategy, select **Create task** next to the strategy.

    The Create task dialog box opens. The **Name**, **Plan** and **Assigned to** fields are required. Assigned to is pre-filled with the assessor, and Priority is pre-filled with 4 - Low. The task starts in the Draft state.

12. To view the complete summary of the assessment, select **View summary**.

13. To check for any errors in the assessment before you submit the assessment, select **Validate** in the header of the project.

    Validation runs and locks editing until it finishes. When it finishes with no errors, the header shows Validation status: Validated and the entity count, for example Entities validated 1/1. A message then reads Validation complete, Assessments were validated. Review the assessment summary before you submit. The Error panel has two tabs, Open and Resolved. Errors are grouped under section headings, such as Inherent assessment, with each error's type, message and status. After you change a response, the header shows Validation status: Needs Validation.

14. Identify the errors and resolve them.

15. Select **Validate** to check if the errors have been resolved.

16. To submit the risk assessment project for approval, select **Submit**, and select **Confirm Submission**.

    Assessments are validated again in this stage. The Submit dialog also has a View summary option. Review the assessment summary before you submit. You can’t make any changes after submission.For a project with multiple entities, **Submit** stays disabled until all the risks across all the scoped entities pass validation.

17. If an assessable entity is retired while the project is in progress, it's automatically removed from the project.

    A note is added to the project's activity log when an entity is removed. If no assessable entities remain in the project, the project is retired.


**Parent Topic:**[Risk assessment project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-risk-management-workspace/risk-assessment-project.md)

