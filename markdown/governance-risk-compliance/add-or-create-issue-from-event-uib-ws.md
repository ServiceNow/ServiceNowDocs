---
title: Add or create an issue from an exercise
description: Add an existing issue or create a new issue to track problems identified during an exercise.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/add-or-create-issue-from-event-uib-ws.html
release: australia
topic_type: task
last_updated: "2026-08-17"
reading_time_minutes: 2
keywords: [BCM, issues, exercise]
breadcrumb: [Structured workflows for Exercises, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Add or create an issue from an exercise

Add an existing issue or create a new issue to track problems identified during an exercise.

## Before you begin

You must have write access to the exercise.

Role required: sn\_recovery.event\_manager, sn\_recovery.event\_user, sn\_bcm.program\_manager

## About this task

The **Issues** related list appears on the exercise record when GRC: Profiles is installed. For more information, see [Managing issues from Business Continuity Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/managing-issues-in-bcm.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace**.

2.  Complete the following steps to create or manage an issue from an exercise.

<table id="choicetable_p55_b3s_jkc"><thead><tr><th align="left" id="d106260e109">

Step

</th><th align="left" id="d106260e112">

Description

</th></tr></thead><tbody><tr><td id="d106260e118">

**Create an issue from the exercise record**

</td><td>

1.  Open the exercise record from the Business Continuity Workspace list view.
2.  Select the **Issues** tab in the record.

If any issues are associated with the exercise record, they are displayed in the **Issues** tab.

\[Omitted image "exercise-form-with-add-new-buttons.png"\] Alt text: Create issue from exercise record.

3.  To create a new issue, select **New**, complete the issue details, and select **Save**.

This step creates a new issue directly from the exercise.

The Create new issue form is shown in the example.

\[Omitted image "create-issue-from-event-record.png"\] Alt text: Create an issue from record.

The classification, issue source, and issue source reference are set automatically. The Issue source is Exercise, classification is Business Continuity Management, and Priority is set to 4-Low.

4.  To add an active issue to the exercise, select **Add** in the record.

Use this option when you want to associate an existing issue with the exercise as an additional source. The exercise is recorded as a secondary source of the issue.

5.  To remove an issue, select it from the list and select **Remove**.

The issue association is removed from the exercise; the issue record isn't deleted from the instance.

</td></tr><tr><td id="d106260e191">

**Link an exercise from the issue record**

</td><td>

1.  Alternately, open the issues list in Business Continuity Workspace list view.
2.  Open an issues record and select the **Exercises** tab.

\[Omitted image "link-exercise-from-issue-record.png"\] Alt text: Link exercise from issue.

3.  To link an exercise from the issue record, select it from the list and select **Add**.


</td></tr></tbody>
</table>3.  Review the issue details in the PDF and Microsoft Word report.

    The Issues section lists the name and description of every issue associated with the exercise. It also shows the state, due date, assigned to, assignment group, priority, and creation date. The following example shows the Issue details in the report.

    \[Omitted image "issues-section-in-pdf.png"\] Alt text: Issue details in the report.


**Parent Topic:**[Structured workflows for Exercises](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/performing-tasks-to-manage-exercise-events.md)

**Related topics**  


[Managing issues from Business Continuity Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/managing-issues-in-bcm.md)

[Dependencies for integrating the Issues module with BCM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/issues-bcm-dependencies.md)

[Add or create an issue from a plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/add-or-create-issue-from-plan-uib-ws.md)

[Report an issue](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/report-grc-issue-frm-plan.md)

