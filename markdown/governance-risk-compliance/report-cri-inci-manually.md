---
title: Report a major incident manually
description: Report a major incident manually in the Digital resilience incident reporting application from the Operational Resilience Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/governance-risk-compliance/report-cri-inci-manually.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Manage, Using Digital resilience incident reporting, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Report a major incident manually

Report a major incident manually in the Digital resilience incident reporting application from the Operational Resilience Workspace.

## Before you begin

Role required: sn\_dri\_inc\_rptg.digital\_resilience\_incident\_manager, sn\_oper\_res.manager

## About this task

Verify that the sn\_dora\_accel\_entity table \(Legal entity for DORA\) contains a record for the financial entity submitting the report. Confirm that sn\_dora\_accel\_third\_party contains records for any ICT third-party providers involved. The Initial report questionnaire references these tables.

## Procedure

1.  Navigate to **Workspaces** &gt; **Operational Resilience Workspace** &gt; **Lists** &gt; **Digital resilience incident reporting** &gt; **All incident reporting cases**.

2.  Select **New**.

3.  Enter the name and description of the incident case record.

4.  On the New record form, fill in the fields and select **Save**.

    Leave the **Source** field set to Manual. To view more information on the fields, see the [Create Digital Resilience Incident form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/create-new-dig-res-inci.md).

    The case is saved in the Draft state, and the Action tasks, Impacted areas, Related areas, Regulations, and Issues tabs are displayed.

5.  If the **Analyst** field is empty and you are a member of the assignment group, select **Accept work**.

6.  Select **Update state**, select In progress in the **State** field, and select **Submit**.

    You can do this step before or after you accept the work on the case.

    The state of the case changes from Draft to In progress.

7.  Open the **Regulations** tab, select **Add**, select the Digital Operational Resilience Act \(DORA\) in the Regulation list, and select **Add**.

    The regulation is listed on the **Regulations** tab with the **Reporting status** To be determined.

    An action task named Regulatory reporting assessment of IT incidents is added to the **Action tasks** tab. The due date of the action task is 1 day from when the regulation is added.

8.  Open the Regulatory reporting assessment of IT incidents action task and select **View assessment** to answer the questions.

    This assessment is used to determine if the incident must be reported to regulatory authorities. Once all answers are provided, the impact on the economy is automatically calculated using the impact automation in the assessment template.

9.  When all required questions are answered, verify the responses and select **Submit**.

    The assessment status changes to Submitted, and the action task moves to the Review state.

10. To complete the action task, when it is in the Review state, select **Update state**, select Closed complete in the **State** field, and select **Submit**.

11. Open the **Regulations** tab of the case and check the **Reporting status** of the regulation.

    You can check whether the auto-calculated regulatory reporting status of the incident is shown as Reportable. The status changes to Reportable when the answers in the assessment meet the reporting criteria. If the criteria are not met, the status does not change to Reportable and the DRI Initial report action task is not created.

12. Open the **Action tasks** tab and check if the DRI Initial report action task has been added for the reportable incident.

    An action task is generated to collect the DRI initial report that should be submitted to the regulator. The due date of the action task is 1 day, or 24 hours, from when the reporting status changes to Reportable. Within this time, the report must be submitted to the authorities.

13. Open the DRI Initial report action task.

    A task owner is required to move an assessment action task to the Assigned state. If the **Task owner** field is empty, assign the action task to yourself or another user in the Assignment section of the **Details** tab. If you accepted the work on the case, new action tasks are assigned to you automatically.

14. Save the action task, select **Update state**, select Assigned in the **State** field, and select **Submit**.

    An action task moves through the Draft, Assigned, Work in progress, Review, and Closed complete states. You move the task from Draft to Assigned and from Assigned to Work in progress, and the task moves to Review after the assessment is submitted. A task in Review can also be closed as Closed incomplete, and a task can be Canceled.

    The action task moves to the Assigned state. The task owner can either reassign or complete the task.

15. To start work on the action task, select **Update state**, select Work in progress in the **State** field, and select **Submit**.

16. Open the **Assessment** tab of the action task, select **View assessment**, and respond to the assessment for the DRI initial report.

    The Assessment Workspace contains DRI assessment templates: Regulatory reporting assessment of IT incidents, and the initial, intermediate, and final report templates. Each action task uses one of these templates to create its assessment. The assessment for the initial report is already created in the **Assessment** tab of the action task, where you can provide incident details. The automation used in the assessment template helps to collect information and calculate responses quickly.

    The date of detection and classification are pre-filled, and some fields are auto-populated. You can automate or manually configure the remaining responses. Once all answers are provided, generate an Excel sheet and submit it to regulatory authorities.

17. To submit the assessment, select **Submit** and generate an Excel sheet.

    You can submit the Excel sheet to the regulatory authorities.

    You can manually add and assign additional action tasks to the owner.

18. When the DRI Initial report action task is in the Review state, select **Update state**, select Closed complete in the **State** field, and select **Submit**.

    When the DRI Initial report action task is completed, a DRI Intermediate report action task is created with a due date of 3 days. A new intermediate report action task is created every 3 days.

19. To add an action task manually, select **New** in Action tasks, enter the name, select the type and the assessment template, and select **Save**.

    Before you move the action task to the Assigned state, enter a due date and an assignment group or a task owner. A task owner is required if the type is Assessment.

20. To export the DRI report, select **Export** &gt; **Export Excel**.

    The export functionality generates a Microsoft Excel sheet based on the reporting cases, which can be saved to your local hard drive and shared with regulatory authorities. You can download the DRI report as shown in the example.

    \[Omitted image "export.png"\] Alt text: Export.

    The Microsoft Excel report contains one tab for each section of the assessment. For the initial report, the tabs are Common details and Initial report. Each tab has the questions as column headers and the answers in the row below.

21. Close all open action tasks, select **Update state**, select Pending approval in the **State** field, and select **Submit**.

    A case moves through the Draft, In progress, Pending approval, Approved, and Closed states, and it can also be Canceled. After the approver approves the case, select **Update state**, select Closed in the **State** field, and select **Submit**. You cannot move the case to Pending approval or Approved while action tasks are open.


