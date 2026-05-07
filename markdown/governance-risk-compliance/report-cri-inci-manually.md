---
title: Report a major incident manually
description: Report a critical incident manually in the Digital resilience incident reporting application from the Operational Resilience Workspace.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Manage, Using Digital resilience incident reporting, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Report a major incident manually

Report a critical incident manually in the Digital resilience incident reporting application from the Operational Resilience Workspace.

## Before you begin

Role required: sn\_dri\_inc\_rptg.digital\_resilience\_incident\_manager, sn\_oper\_res.manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Operational Resilience Workspace** &gt; **Digital resilience incident reporting** &gt; **All incident reporting cases**.

2.  Select **New**.

3.  Enter the name and description of the incident case record.

4.  On the New record form, fill in the fields.

    To view more information on the fields, see the [Create New Digital Resilience Incident form](../reference/create-new-dig-res-inci.md).

5.  Select **Accept work**.

6.  Monitor how the status of the incident has changed once the answers are provided in the questionnaire.

    Once all answers are provided, the impact on the economy is automatically calculated using the impact automation in the assessment template.

7.  To submit the response to the questionnaire as an analyst, verify the responses and select **Submit**.

    A confirmation message is displayed that the answers are submitted successfully.

8.  Navigate to the **Details** tab of the incident and check the reporting status.

    You can check whether the auto-calculated regulatory reporting status of the incident is shown as Reportable.

9.  Navigate to the **Action tasks** tab and check if an action task has been added for the reportable incident.

    An action task is generated to collect the DRI initial report that should be submitted to the regulator.

10. Navigate to the DRI initial report action task in the incident and assign the action task to themselves or another user in the Assignment section of the **Details** tab.

11. Save the action task, select **Update state**, and select **Submit**.

    The action task is assigned to the user and the Task owner field is locked on the form. The user can either reassign or complete the task. A due date is provided for the action task which is a 1-day time, 24 hours from when the incident got classified as major. Within the next 24 hours, this report must be submitted to the authorities.

12. Navigate to the **Assessment** tab and respond to the assessment for DRI initial report.

    The first assessment, which is the regulatory reporting assessment, is used to determine if the incident must be reported to regulatory authorities. For reportable incidents, three assessment templates are created for the initial, intermediate, and final report in the Assessment Workspace.

    In this case, an assessment is already created in the **Assessment** tab of the action task, where you can provide incident details. The automation used in the assessment template helps to collect information and calculate responses quickly.

    The date of detection and classification are pre-filled, and some fields are auto-populated. You can automate or manually configure the remaining responses. Once all answers are provided, generate an Excel sheet and submit it to regulatory authorities.

13. To submit the assessment, select **Submit** and generate an Excel sheet.

    You can submit the Excel sheet to the regulatory authorities.

    The initial report is automatically generated, and an intermediate report is created every third day the incident remains open. Once the incident is closed or resolved in Incident Management, it is moved to a Closed status.

    Action tasks are automatically added to the incident, and you can manually add and assign additional tasks to the owner.

14. To add an action task manually, select **New** in Action tasks.

15. To export and download the DRI report, select **Export**, add the file name, and select **Save**.

    The export functionality generates a Microsoft Excel sheet based on the reporting cases, which can be saved to your local hard drive and shared with regulatory authorities. You can download the DRI report as shown in the example.

    ![Export.](../image/export.png)

    The Microsoft Excel report contains the Common details and Initial report tabs. All fields from the initial report are exported with their names as column headers.

16. To save the case record, select **Save**.


