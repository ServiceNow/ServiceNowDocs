---
title: Add or create an issue from a crisis event
description: Add an existing issue or create an issue to track problems identified during a crisis event.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/add-or-create-issue-from-crisis-event.html
release: zurich
topic_type: task
last_updated: "2026-08-23"
reading_time_minutes: 2
breadcrumb: [Structured workflows for crisis events, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Add or create an issue from a crisis event

Add an existing issue or create an issue to track problems identified during a crisis event.

## Before you begin

Role required: sn\_recovery.event\_manager, sn\_recovery.event\_user, sn\_bcm.program\_manager

The **Issues** related list appears on a crisis event record when GRC: Profiles is installed. For more information, see [Managing issues from Business Continuity Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/managing-issues-in-bcm.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace**.

2.  Complete the following steps to create or manage an issue from a crisis event.

<table id="choicetable_p55_b3s_jkc"><thead><tr><th align="left" id="d318218e97">

Step

</th><th align="left" id="d318218e100">

Description

</th></tr></thead><tbody><tr><td id="d318218e106">

**Create or add an issue from the event record**

</td><td>

1.  Open the crisis event record from the Business Continuity Workspace list view.
2.  Select the **Issues** tab in the record.

It shows the issues associated with the crisis event.

\[Omitted image "event-form-with-add-new-buttons.png"\] Alt text: Event form with Add and New buttons.

3.  To create a new issue, select **New**, complete the issue details, and select **Save**.

This step creates a new issue directly from the crisis event.

The Create new issue form is shown in the example.

\[Omitted image "create-new-issue-from-event.png"\] Alt text: Create an issue from event record.

The classification, issue source, and issue source reference are set automatically. The Issue source is Crisis event, classification is Business Continuity Management, and Priority is set to 2-High by default.

4.  To add an active issue to the event, select **Add** in the record.

Use this option when you want to associate an existing issue with the crisis event as an additional source. The event is recorded as a secondary source of the issue.

\[Omitted image "add-button-event.png"\] Alt text: Add button in Crisis event record.

5.  To remove an issue, select it from the list and select **Remove**.

The issue association is removed from the event; the issue record isn't deleted from the instance.

</td></tr><tr><td id="d318218e181">

**Link a crisis event from the issue record**

</td><td>

1.  Alternately, open the issues list in Business Continuity Workspace list view.
2.  Open an issues record and select the **Crisis events** tab.

\[Omitted image "add-crisis-event-from-issue-record.png"\] Alt text: Add Crisis event from issue record.

3.  To link a crisis event from the issue record, select an event from the list and select **Add**.


</td></tr></tbody>
</table>3.  Review the issue details in the PDF and Microsoft Word report.

    The Issues section lists the name and description of every issue associated with the event. It also shows the state, due date, assigned to, assignment group, priority, and creation date. The following example shows the Issue details in the report.

    \[Omitted image "issues-section-in-pdf-events.png"\] Alt text: Issues section in the PDF.


**Parent Topic:**[Structured workflows for crisis events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/perform-tasks-to-manage-crisis-events.md)

