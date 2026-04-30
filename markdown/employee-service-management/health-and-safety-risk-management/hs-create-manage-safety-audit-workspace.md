---
title: Create and manage a safety audit
description: Create a safety audit for a process or regulation with formalized assessment criteria, and record the information collected at each stage—before, during, and after the audit.
locale: en-US
release: yokohama
product: Health and Safety Risk Management
classification: health-and-safety-risk-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Safety inspections and audits, Use, Health and Safety Risk Management, Health and Safety, Employee Service Management]
---

# Create and manage a safety audit

Create a safety audit for a process or regulation with formalized assessment criteria, and record the information collected at each stage—before, during, and after the audit.

## Before you begin

Role required: sn\_hs\_rm.safety\_audit\_manager or sn\_hs\_rm.safety\_audit\_writer

## About this task

You can also set up an audit schedule to generate safety audits. For more information, see [Set up a safety audit schedule](hs-setup-safety-audit-schedule.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Health and Safety Workspace**.

2.  Select the risk management icon \(![Risk assessment icon](../image/icon-risk-assessment.png)\).

3.  Select the **Audits** list and then **All**.

4.  Select **New** to create an audit.

    Alternatively, you can create an audit from

    -   The **Scheduled audits** tab in an audit schedule.
    -   The **Create audits** button that appears when a new audit schedule is saved.
5.  On the form, fill in the fields.

    Enter details such as the audit scope, its goals, regulation for the audit, and a start and end date.

    For information on audit field descriptions, see [Audit schedule form](../reference/hs-audit-schedule-form.md).

6.  Select **Save**.

    The **People involved**, **Documents**, **Audit surveys**, **Findings**, **Risk assessments**, **Observations**, and **Audit actions** tabs appear for this audit.

7.  In the **People involved** tab, select **New** to add people involved in this audit and their responsibilities.

    **Note:**

    -   The **Visitors involved** field appears only when the Workplace Visitor Management \(com.sn\_wsd\_visitor\) application is installed on your instance. For more information, see [Additional features in Health and Safety](../../ohs-incident-management/task/install-hs-incident-mgmt.md#table_ix1_bff_gxb).
    -   The **Contractor** option appears only when the Health and Safety Contractor Management \(sn\_hs\_crm\) application is installed on your instance. The field only lists users who have the \[snc\_external\] role assigned to them and have their Health and Safety profile created. For more information, see [Assign Health and Safety profile to a user](../../ohs-incident-management/task/assign-hs-profile-user.md).
8.  In the **Documents** tab, add standards and documents used to benchmark findings.

    -   Select **Add** to add existing documents.
    -   Select **New** to upload new documents. For field descriptions, see [Health and Safety document version form](../../ohs-incident-management/reference/hs-document-form.md).
9.  In the **Audit surveys** tab, add and assign smart assessments or surveys to be conducted as part of this audit.

    If the audit is part of an audit schedule with an associated audit survey, that survey is automatically added to the audit record. For information on audit survey field descriptions, see [Audit survey form](../reference/hs-audit-survey-form.md).

    -   The assigned user receives a notification to complete the smart assessment or survey.
    -   A smart assessment can be completed in the mobile app. For more information, see [Complete a smart assessment from mobile](../../hs-health-safety-mobile/task/hs-create-smart-assessment-inspection-audit-mobile-agent.md).
    -   A survey can be completed either through the Employee Center or on the mobile app. For more information, see [Complete a survey from the Employee Center](hs-complete-safety-insp-survey.md).
10. Review the survey responses and gather evidence as part of the audit, for example, document assessments, interviews, and observations.

    1.  In the **Audit surveys** tab of a survey, review the the smart assessment or survey responses that are submitted by the assigned user.

        When completed, the assessment results are available in the following tabs:

        -   **Questionnaire results** tab for a smart assessment.
        -   **Audit survey results** tab for an inspection survey.
    2.  In the **Findings** tab, add an audit finding gathered from survey responses and perform its root cause analysis.

        For more information, see [Add a finding and root cause analysis for a safety audit](hs-add-finding-rca-safety-audit.md).

        **Note:** Safety auditors can also create actions and findings for specific questions while completing a smart assessment or survey in the mobile app. When an agent creates an action for a question, the system also generates a related finding record based on the response. The finding then appears in this tab in the workspace. For more information, see [Create actions and findings for the smart assessment questionnaire from mobile app](../../hs-health-safety-mobile/task/hs-create-actions-findings-smart-assessments.md).

    3.  In the **Risk assessments** tab, select **New** to conduct a risk assessment as part of this audit.

        -   Alternatively, select **Add** to associate an existing risk assessment to the audit record.
        -   For more information, see [Conduct a safety risk assessment](hs-conduct-risk-assessment.md).
    4.  In the **Observations** tab, add an observation recorded from this audit.

        -   Select **Add** to add an existing observation.
        -   Select **New** to create and submit a new observation.
    5.  In the **Audit actions** tab, select **New** to create and assign any actions based on findings and recommendations.

        For more information, see [Add an action for a safety inspection or audit](hs-add-action-safety-inspection.md).

        **Note:** Any actions created for specific questions while completing the smart assessment or survey in the Employee Center or mobile app also appear in this tab.

11. If needed, complete the audit surveys directly from the audit record in the workspace.

    1.  Open the assessment to be completed.

        -   For a smart assessment, select **Open audit smart assessment**.

            **Note:** Only a user with the **Assessment reader role** can access and complete this smart assessment. This role is set during the smart assessment template configuration. For more information, see [Configure the smart assessment template for safety inspections and audits](hs-configure-smart-assessment-template.md).

        -   For an inspection survey, select **Open audit survey**.
    2.  Answer the survey questions and select **Submit**.

    3.  In the **State** field, select Closed Complete to close the audit survey.

12. In the **Details** tab, set the state to Closed Complete after all audit activities are complete and then select **Save**.

    The audit moves to the Closed Complete state.

13. Generate a report for the safety audit, if needed.

    1.  Select **Generate report**.

        **Note:** The **Generate report** button appears only when the Audit \[sn\_hs\_rm\_audit\] table is enabled for report field mapping. For more information, see [Enable a Health and Safety table for configuring report field mapping](../../ohs-incident-management/task/enable-hs-table-report-field-mapping.md).

    2.  In the **Generate report** dialog box, select a report mapping in the **Select report** field.

        Only the report mapping forms created and published for the Audit \[sn\_hs\_rm\_audit\] table are available to select in the **Select report** field. For more information, see [Create a safety report field mapping for generating reports](../../ohs-incident-management/task/create-safety-report-field-mapping.md).

    3.  Select **Generate**.


**Parent Topic:**[Safety inspections and audits](../concept/hs-safety-inspections.md)

