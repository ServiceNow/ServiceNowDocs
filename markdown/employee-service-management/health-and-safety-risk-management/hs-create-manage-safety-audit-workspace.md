---
title: Create and manage a safety audit
description: Create a safety audit for a process or regulation with formalized assessment criteria, and record the information collected at each stage—before, during, and after the audit.
locale: en-US
release: zurich
product: Health and Safety Risk Management
classification: health-and-safety-risk-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Safety inspections and audits, Use, Health and Safety Risk Management, Health and Safety, Employee Service Management]
---

# Create and manage a safety audit

Create a safety audit for a process or regulation with formalized assessment criteria, and record the information collected at each stage—before, during, and after the audit.

## Before you begin

Role required: sn\_hs\_rm.safety\_audit\_manager or sn\_hs\_rm.safety\_audit\_writer

## About this task

You can also set up an audit schedule to generate recurring safety audits. For more information, see [Set up a safety audit schedule](hs-setup-safety-audit-schedule.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Health and Safety Workspace**.

2.  Select the risk management icon \(![Risk assessment icon](../image/icon-risk-assessment.png)\).

3.  Select the **Audits** list and then **All**.

4.  Select **New** and then select an audit creation method.

<table id="choicetable_ll2_jw3_l3c"><thead><tr><th align="left" id="d559732e111">

Option

</th><th align="left" id="d559732e114">

Steps

</th></tr></thead><tbody><tr><td id="d559732e120">

**Add to audit schedule**

</td><td>

Select this option to create this audit as part of an existing audit schedule.1.  In the **Audit schedule** field, select the audit schedule to add this audit record to.
2.  Select **Create**.


</td></tr><tr><td id="d559732e143">

**Standalone audit**

</td><td>

Select this option to create an independent audit. 1.  In the **Regulatory audit** field, indicate the audit's regulatory status.
2.  Enter short description and audit goals.
3.  Select **Create**.


</td></tr></tbody>
</table>    The **Overview**, **Details**, **Objectives**, **People involved**, **Documents**, **Audit questionnaires**, **Findings**, **Risk assessments**, **Audit actions**, **Audit schedule**, **Approvers**, and **Results** tabs appear for this audit.

5.  In the **Details** tab, fill in the fields.

    Enter details such as the audit scope, its goals, regulation for the audit, and a start and end date.

    For information on audit field descriptions, see [Audit schedule form](../reference/hs-audit-schedule-form.md).

6.  In the **People involved** tab, add people involved in this audit and their responsibilities.

    For more information, see [Add people involved in a safety audit](hs-add-people-involved-safety-audit.md).

7.  In the **Objectives** tab, define the audit objectives, the criteria used as benchmarks, and the items to be reviewed for this audit.

    -   For more information, see [Define an objective for a safety audit](hs-define-safety-audit-objectives.md).
    -   Alternatively, if you have a previous audit with a similar scope, select **Import scope** to pre-populate these sections rather than entering them manually. For more information, see [Import scope from an existing safety audit](hs-import-scope-existing-safety-audit.md).
8.  In the **Documents** tab, add standards and documents used to benchmark findings.

    -   Select **Add** to add an existing document from Health and Safety document library.
    -   Select **New** to upload a new document. For field descriptions, see [Health and Safety document version form](../../ohs-incident-management/reference/hs-document-form.md).
9.  In the **Audit questionnaires** tab, add and assign smart assessments or surveys to be conducted as part of this audit.

    If the audit is part of an audit schedule with an associated audit questionnaire, that questionnaire is automatically added to the audit record. For information on audit questionnaire field descriptions, see [Audit questionnaire form](../reference/hs-audit-survey-form.md).

    -   The assigned user receives a notification to complete the smart assessment or survey.
    -   A smart assessment can be completed in the mobile app. For more information, see [Complete a smart assessment from mobile](../../hs-health-safety-mobile/task/hs-create-smart-assessment-inspection-audit-mobile-agent.md).
    -   A survey can be completed either through the Employee Center or on the mobile app. For more information, see [Complete a survey from the Employee Center](hs-complete-safety-insp-survey.md).
10. Conduct the audit and gather evidence as part of the audit, for example, document assessments, interviews, and observations.

    1.  In the **Audit questionnaires** tab, review the the smart assessment or survey responses that are submitted by the assigned user.

        When completed, the assessment results are available in the **Audit questionnaire results** tab.

    2.  In the **Findings** tab, record findings for audit's items for review.

        For more information, see [Add a finding for a review item in a safety audit](hs-add-finding-rca-safety-audit.md).

        **Note:** Safety auditors can also create actions and findings for specific questions while completing a smart assessment in the mobile app. When an agent creates an action for a question, the system also generates a related finding record based on the response. The finding then appears in this tab in the workspace. For more information, see [Create actions and findings for the smart assessment questionnaire from mobile app](../../hs-health-safety-mobile/task/hs-create-actions-findings-smart-assessments.md).

    3.  In the **Risk assessments** tab, select **New** to conduct a risk assessment as part of this audit.

        -   Alternatively, select **Add** to associate an existing risk assessment to the audit record.
        -   For more information, see [Conduct a safety risk assessment](hs-conduct-risk-assessment.md).
    4.  In the **Audit actions** tab, create and assign any actions based on findings and recommendations.

        For more information, see [Add an action for a safety audit](hs-add-action-safety-inspection.md).

        **Note:** Any actions created for specific questions while completing the smart assessment or survey in the Employee Center or mobile app also appear in this tab.

11. If needed, complete the audit surveys directly from the audit record in the workspace.

    1.  Open the assessment to be completed.

        -   For a smart assessment, select **Open audit smart assessment**.

            **Note:** Only a user with the **Assessment reader role** can access and complete this smart assessment. This role is set during the smart assessment template configuration. For more information, see [Configure the smart assessment template for safety inspections and audits](hs-configure-smart-assessment-template.md).

        -   For an inspection survey, select **Open audit survey**.
    2.  Answer the survey questions and select **Submit**.

    3.  In the **State** field, select Closed Complete to close the audit survey.

12. In the **Overview** tab, review the audit progress and metrics.

    For more information, see [Monitor safety audit progress and outcomes at a glance](hs-view-safety-audit-progress.md).

13. If necessary, submit the safety audit, findings, actions, or results for approval.

    For more information, see [Submit a safety audit, finding, or action for approval](hs-submit-audit-finding-action-approval.md).

14. In the **Results** tab, record the audit result and compare them with previous audits.

    For more information, see [Record safety audit results](hs-review-results-compare-with-previous-audits.md).

15. In the **Details** tab, set the state to Closed Complete after all audit activities and objectives are complete, and then select **Save**.

    The audit moves to the Closed Complete state.


## What to do next

If needed, generate a report for the safety audit.

1.  Select **Generate report**.

    **Note:** The **Generate report** button appears only when the Audit \[sn\_hs\_rm\_audit\] table is enabled for report field mapping. For more information, see [Enable a Health and Safety table for configuring report field mapping](../../ohs-incident-management/task/enable-hs-table-report-field-mapping.md).

2.  In the **Generate report** dialog box, select a report mapping in the **Select report** field.

    Only the report mapping forms created and published for the Audit \[sn\_hs\_rm\_audit\] table are available to select in the **Select report** field. For more information, see [Create a safety report field mapping for generating reports](../../ohs-incident-management/task/create-safety-report-field-mapping.md).

3.  Select **Generate**.

-   **[Add people involved in a safety audit](hs-add-people-involved-safety-audit.md)**  
Add people involved to record all participants in a safety audit — their roles, responsibilities, and the objectives and actions assigned to them.
-   **[Define an objective for a safety audit](hs-define-safety-audit-objectives.md)**  
Define an objective to add detailed goal and scope of the safety audit. You can create as many objectives as the audit requires.
-   **[Import scope from an existing safety audit](hs-import-scope-existing-safety-audit.md)**  
Import scope to copy the audit details, people involved, and objectives \(including criteria and items for review\) from an existing audit.
-   **[Add a finding for a review item in a safety audit](hs-add-finding-rca-safety-audit.md)**  
Record a finding for a review item during an audit and perform a root cause analysis \(RCA\) for it.
-   **[Monitor safety audit progress and outcomes at a glance](hs-view-safety-audit-progress.md)**  
Use the **Overview** tab in a Health and Safety audit to quickly assess the audit completion status and outstanding items.
-   **[Submit a safety audit, finding, or action for approval](hs-submit-audit-finding-action-approval.md)**  
When completed, submit the safety audit, finding, or action for approval and start the approval workflow.
-   **[Record safety audit results and compare with previous audits](hs-review-results-compare-with-previous-audits.md)**  
Record the audit result and outcomes and compare them with previous audits to identify trends and track progress over time.

**Parent Topic:**[Safety inspections and audits](../concept/hs-safety-inspections.md)

