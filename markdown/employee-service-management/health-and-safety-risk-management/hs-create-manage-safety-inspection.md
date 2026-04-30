---
title: Create and manage a safety inspection
description: Create a safety inspection to manage your workplace inspection of a particular activity, process, or an area. Review the questionnaire responses and add findings, root cause analyses \(RCA\), and actions for the inspection.
locale: en-US
release: yokohama
product: Health and Safety Risk Management
classification: health-and-safety-risk-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Safety inspections and audits, Use, Health and Safety Risk Management, Health and Safety, Employee Service Management]
---

# Create and manage a safety inspection

Create a safety inspection to manage your workplace inspection of a particular activity, process, or an area. Review the questionnaire responses and add findings, root cause analyses \(RCA\), and actions for the inspection.

## Before you begin

Role required: sn\_hs\_rm.safety\_inspection\_manager or sn\_hs\_rm.safety\_inspection\_writer

## About this task

You can also set up an inspection schedule to schedule recurring safety inspections. For more information, see [Set up a safety inspection schedule](hs-schedule-recurring-safety-inspection.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Health and Safety Workspace**.

2.  Select the risk management icon \(![Risk assessment icon](../image/icon-risk-assessment.png)\).

3.  Select the **Inspections** list and then **All**.

4.  Select **New** to create an inspection.

5.  On the form, fill in the fields.

    Enter details such as inspection format, smart assessment or survey to use for this inspection, risk matrix used for risk assessments for this inspection, and a due date to complete the inspection.

    For more information on inspection field descriptions, see [Inspection schedule form](../reference/hs-inspection-schedule-form.md).

6.  Select **Save**.

    -   Based on the **Assessment type** field, the following tabs appear for this inspection:
        -   For a smart assessment: **Questionnaire results**, **Findings and RCA**, and **Inspection actions**.
        -   For an inspection survey: **Inspection survey results**, **Findings and RCA**, and **Inspection actions**.
    -   The associated smart assessment or inspection survey is assigned for completion.
    -   The assigned user receives a notification to complete the smart assessment or survey. If the inspection format is digital, the notification includes a direct link to access the assessment or survey.
        -   A smart assessment can be completed from the mobile app. For more information, see [Complete a smart assessment from mobile](../../hs-health-safety-mobile/task/hs-create-smart-assessment-inspection-audit-mobile-agent.md).
        -   A survey can be completed either in the Employee Center or the mobile app. For more information, see [Complete an inspection survey from the Employee Center](hs-complete-safety-insp-survey.md).
7.  Review the smart assessment or inspection survey responses that are submitted by the assigned user.

    When completed, the assessment results for this inspection are available in the following tabs:

    -   **Questionnaire results** tab for a smart assessment.
    -   **Inspection survey results** tab for an inspection survey.
8.  If needed, complete the assessment directly from the inspection record in the workspace.

    -   For a smart assessment, select **Open inspection smart assessment**.

        **Note:** Only a user with the **Assessment reader role** can access and complete this smart assessment. This role is set during the smart assessment template configuration. For more information, see [Configure the smart assessment template for safety inspections and audits](hs-configure-smart-assessment-template.md).

    -   For an inspection survey, select **Open inspection survey**.
    These buttons appear only when the **Inspection format** is set to **Digital**.

9.  In the **Findings and RCA** tab, work on the inspection findings, and perform an RCA for this inspection.

    For more information, see [Add a finding and root cause analysis for a safety inspection](hs-add-finding-rca-safety-inspection.md).

    **Note:** Inspection agents can also create actions and findings for specific questions while completing a smart assessment or survey in the mobile app. When an agent creates an action for a question, the system also generates a related finding record based on the response. The finding then appears in this tab in workspace. For more information, see [Create actions and findings for the smart assessment questionnaire from mobile app](../../hs-health-safety-mobile/task/hs-create-actions-findings-smart-assessments.md).

10. If applicable, add actions for findings in the **Inspection actions** tab.

    For more information, see [Add an action for a safety inspection or audit](hs-add-action-safety-inspection.md).

    **Note:** Any actions created for specific questions while completing the smart assessment or survey in the Employee Center or mobile app also appear in this tab.

11. In the **Details** tab, set the state to Closed Complete after all inspection activities are complete and then select **Save**.

    The inspection moves to the Closed Complete state.


**Parent Topic:**[Safety inspections and audits](../concept/hs-safety-inspections.md)

