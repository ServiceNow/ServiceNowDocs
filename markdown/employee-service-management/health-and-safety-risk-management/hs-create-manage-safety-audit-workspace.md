---
title: Create and manage a safety audit
description: Create a safety audit for a process or regulation with formalized assessment criteria, and record the information collected at each stage—before, during, and after the audit.
locale: en-US
release: xanadu
product: Health and Safety Risk Management
classification: health-and-safety-risk-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Safety inspections and audits, Use, Health and Safety Risk Management, Health and Safety, Employee Service Management]
---

# Create and manage a safety audit

Create a safety audit for a process or regulation with formalized assessment criteria, and record the information collected at each stage—before, during, and after the audit.

## Before you begin

Role required: sn\_hs\_rm.safety\_audit\_manager or sn\_hs\_rm.safety\_audit\_writer

## About this task

You can also set up an audit schedule to create safety audits. For more information, see [Set up a safety audit schedule](hs-setup-safety-audit-schedule.md).

## Procedure

1.  Navigate to **All** &gt; **Health and Safety** &gt; **Health and Safety Workspace**.

2.  Select the risk management icon \(![Risk assessment icon](../image/icon-risk-assessment.png)\).

3.  Select the **Audits** list and then **All**.

4.  Select **New** to create an audit.

    Alternatively, you can open an audit from

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
    -   Select **New** to upload new documents. For field descriptions, see [Health and Safety document form](../../ohs-incident-management/reference/hs-document-form.md).
9.  In the **Audit surveys** tab, add and assign audit surveys to be conducted as part of this audit.

    Only the surveys with the **Source table** field set to Audit survey \[sn\_hs\_rm\_audit\_survey\] table are available in this list. For more information, see [Configure a safety inspection or audit survey](hs-configure-safety-inspection-surveys.md).

10. If needed, complete the audit surveys in this audit record.

    1.  Open the audit survey to be completed and select **Open audit survey**.

    2.  Answer the survey questions and select **Submit**.

        When completed, the survey results are available in the **Audit survey results** tab of this audit survey.

    3.  Add action to the survey responses if needed.

    4.  In the **State** field on the audit form, select Closed Complete to close the survey.

    **Note:** An auditor can also complete the audit survey through Employee Center or on Now Mobile app. For more information, [Complete a safety audit survey through Employee Center](hs-complete-safety-insp-survey.md).

11. Review the survey responses and gather evidence as part of the audit, for example, document assessments, interviews, and observations.

    1.  In the **Audit surveys** tab of a survey, review the survey responses.

    2.  In the **Findings** tab, add an audit finding gathered from survey responses and perform its root cause analysis.

        For more information, see [Add a finding and root cause analysis for a safety audit](hs-add-finding-rca-safety-audit.md).

    3.  In the **Risk assessments** tab, select **New** to conduct a risk assessment as part of this audit.

        -   You can also select **Add** to associate an existing risk assessment to the audit record.
        -   For more information, see [Conduct a safety risk assessment](hs-conduct-risk-assessment.md).
    4.  In the **Observations** tab, add an observation recorded from this audit.

        -   Select **Add** to add an existing observation.
        -   Select **New** to create and submit a new observation.
    5.  In the **Audit actions** tab, select **New** to create and assign any actions based on findings and recommendations.

        For field descriptions, see [Health and Safety action form](../../ohs-incident-management/reference/hs-action-form.md).

12. Generate a report for the safety audit, if needed.

    1.  Select **Generate report**.

        **Note:** The **Generate report** button appears only when the Audit \[sn\_hs\_rm\_audit\] table is enabled for report field mapping. For more information, see [Enable a Health and Safety table for configuring report field mapping](../../ohs-incident-management/task/enable-hs-table-report-field-mapping.md).

    2.  In the **Generate report** dialog box, select a report mapping in the **Select report** field.

        Only the report mapping forms created and published for the Audit \[sn\_hs\_rm\_audit\] table are available to select in the **Select report** field. For more information, see [Create a safety report field mapping](../../ohs-incident-management/task/create-safety-report-field-mapping.md).

    3.  Select **Generate**.

13. In the **Details** tab, set the state to Closed Complete after all audit activities are complete and then select **Save**.

    In a closed complete state, no further changes can be made to the **People involved**, **Audit surveys**, **Findings**, **Risk assessments**, and **Observations** related items in an audit record.

    The audit moves to the Closed Complete state.


**Parent Topic:**[Safety inspections and audits](../concept/hs-safety-inspections.md)

