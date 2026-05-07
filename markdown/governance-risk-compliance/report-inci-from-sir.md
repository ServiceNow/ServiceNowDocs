---
title: Report a major incident from Security Incident Response
description: Report a critical incident from Security Incident Response in the Digital resilience incident reporting application.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Reporting incidents from SOW and SIR Workspace in DRIR, Manage, Using Digital resilience incident reporting, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Report a major incident from Security Incident Response

Report a critical incident from Security Incident Response in the Digital resilience incident reporting application.

## Before you begin

Role required: sn\_dri\_inc\_rptg.digital\_resilience\_incident\_manager

## About this task

Security Incident Response reporting workflow consists of the following steps:

1.  Create an incident report from Security Incident Response.
2.  Copy the impacted areas from the source tables.
3.  Create action tasks and regulatory assessments for the initial, intermediate, and final reports.
4.  Respond to the assessments and populate the responses.
5.  Configure the rules engine to automatically update the regulatory status on the incident reporting case.
6.  Extract the reports in Microsoft Excel format for the regulators.

## Procedure

1.  Navigate to **Workspaces** &gt; **Operational Resilience Workspace** &gt; **Digital resilience incident reporting** &gt; **All incident reporting cases**.

2.  Open the Digital resilience incident case from the list view.

    The following example shows the Digital resilience incident case generated from the Security Incident Response application.

    The source of the case is SIR.

    ![SIR.](../image/src-sir.png)

    The case is assigned to the Digital Resilience Incident Managers group.

    The action tasks related to the incident are copied in the case record.

    An action task is automatically generated for the incident to help you determine if it must be reported to regulatory bodies. When you open the action task, you can view its name, description, type, and the associated assessment template. This template, created by the administrator, is already available in the Assessment Workspace, where you can view its sections and questions.

    The assessment template is aligned with the Digital Operational Resilience classification for major Information and Communication Technology \(ICT\) incidents. The same assessment template is tagged in the reported incident.

    The analyst assigned to the case assesses the incident's impact on factors such as critical services, clients \(including financial counterparts and third parties\), data and data losses, reputation, service downtime, geographical spread, and economy. These sections in the template help you determine the impact of the incident and whether it should be reported to the regulators and responds to the questions in the questionnaire. For information on the assessment template, see [Create an assessment template](../../assessment-engine/task/sae-asmnt-template-create.md).

3.  Select **Accept work**.

4.  Monitor how the status of the incident has changed once the answers are provided in the questionnaire.

    Once all answers are provided, the impact on the economy is automatically calculated using the impact automation in the assessment template.

5.  To submit the response to the questionnaire as an analyst, verify the responses and select **Submit**.

    A confirmation message is displayed that the answers are submitted successfully.

6.  Navigate to the **Details** tab of the incident and check the reporting status.

    You can check whether the auto-calculated regulatory reporting status of the incident is shown as Reportable.

7.  Navigate to the **Action tasks** tab and check if an action task has been added for the reportable incident.

    An action task is generated to collect the DRI initial report that should be submitted to the regulator.

8.  Navigate to the DRI initial report action task in the incident and assign the action task to themselves or another user in the Assignment section of the **Details** tab.

9.  Save the action task, select **Update state**, and select **Submit**.

    The action task is assigned to the user and the Task owner field is locked on the form. The user can either reassign or complete the task. A due date is provided for the action task which is a 1-day time, 24 hours from when the incident got classified as major. Within the next 24 hours, this report must be submitted to the authorities.

10. Navigate to the **Assessment** tab and respond to the assessment for DRI initial report.

    The first assessment, which is the regulatory reporting assessment, is used to determine if the incident needs to be reported to regulatory authorities. For reportable incidents, three assessment templates are created for the initial, intermediate, and final report in the Assessment Workspace.

    In this case, an assessment is already created in the **Assessment** tab of the action task, where you can provide incident details. Automation used in the assessment template helps to collect information and calculate responses quickly.

    The date of detection and classification are pre-filled, and some fields are auto-populated. You can automate or manually configure the remaining responses. Once all answers are provided, generate an Excel sheet and submit it to regulatory authorities.

11. To submit the assessment, select **Submit** and generate an Excel sheet.

    You can submit the Excel sheet to the regulatory authorities.

    The initial report is automatically generated, and an intermediate report is created every third day the incident remains open. Once the incident is closed or resolved in Incident Management, it is moved to a Closed status, and a final report is generated with a due date of 30 days.

    Action tasks are automatically added to the incident, and you can manually add and assign additional tasks to the owner.

12. To add an action task manually, select **New** in Action tasks and complete its workflow.

13. To export and download the DRI report, select **Export**, add the file name, and select **Save**.

    The export functionality generates a Microsoft Excel sheet based on the reporting cases, which can be saved to your local hard drive and shared with regulatory authorities. You can download the DRI report as shown in the example.

    ![Export.](../image/export.png)

    The Microsoft Excel report contains the Common details and Initial report tabs. All fields from the initial report are exported with their names as column headers.

14. To save the case record, select **Save**.


