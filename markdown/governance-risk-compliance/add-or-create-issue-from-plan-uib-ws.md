---
title: Add or create an issue from a plan
description: Add an existing issue or create an issue from a business continuity plan to track problems identified during continuity planning.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/add-or-create-issue-from-plan-uib-ws.html
release: zurich
topic_type: task
last_updated: "2026-08-17"
reading_time_minutes: 2
keywords: [BCM, issues, plan]
breadcrumb: [Structured workflows for BCPs, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Add or create an issue from a plan

Add an existing issue or create an issue from a business continuity plan to track problems identified during continuity planning.

## Before you begin

You must have write access to the business continuity plan.

Role required: sn\_bcp.plan\_contributor, sn\_bcp.plan\_manager, or sn\_bcm.program\_manager

## About this task

The **Issues** related list appears on a plan record when GRC: Profiles is installed. For more information, see [Managing issues from Business Continuity Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/managing-issues-in-bcm.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace**.

2.  Complete the following steps to create or manage an issue from a plan record.

<table id="choicetable_p55_b3s_jkc"><thead><tr><th align="left" id="d287612e109">

Step

</th><th align="left" id="d287612e112">

Description

</th></tr></thead><tbody><tr><td id="d287612e118">

**Create or add an issue from the plan record**

</td><td>

1.  Open the plan record from the Business Continuity Workspace list view.
2.  Select the **Issues** tab in the record.

The **Issues** related list shows the issues associated with the plan.

\[Omitted image "issues-related-list-plan.png"\] Alt text: Issues related list on a business continuity plan with the Add and New actions.

3.  To create a new issue, select **New**, complete the issue details, and select **Save**.

This step creates a new issue directly from the plan.

The Create new issue form is shown in the example.

\[Omitted image "create-issue-from-plan-record.png"\] Alt text: Create an issue from plan record.

The classification, issue source, and issue source reference are set automatically.

4.  To add an active issue to the plan, select **Add** in the record.

Use this option when you want to associate an existing issue with the plan as an additional source. The plan is recorded as a secondary source of the issue.

\[Omitted image "add-issue-from-plan.png"\] Alt text: Add issue from plan record.

5.  To remove an issue, select it from the list and choose **Remove**.

The issue association is removed from the plan; the issue record isn't deleted from the instance.

</td></tr><tr><td id="d287612e193">

**Link a plan from the issue record**

</td><td>

1.  Open the issues list in Business Continuity Workspace list view.
2.  Open an issue record and select the **Plans** tab.
3.  To link a plan from the issue record, select it from the list and select **Add**.

\[Omitted image "add-plans-to-the-issue-record.png"\] Alt text: Add plans to the Issue record.

</td></tr></tbody>
</table>3.  Review the issue details in the PDF and Microsoft Word report.

    The Issues section lists the name and description of every issue associated with the plan. It also shows the state, due date, assigned to, assignment group, priority, and creation date. In the report, the Issues section appears after the recovery tasks section and before the contributors and attachments sections. The following example shows the Issue details in the Plan report.

    \[Omitted image "pdf-template-updated-to-include-issues-section.png"\] Alt text: Issue details in the Plan report.


**Parent Topic:**[Structured workflows for BCPs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/bcp-tasks-performed-by-bcp-owner.md)

**Related topics**  


[Managing issues from Business Continuity Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/managing-issues-in-bcm.md)

[Dependencies for integrating the Issues module with BCM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/issues-bcm-dependencies.md)

[Add or create an issue from an exercise](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/add-or-create-issue-from-event-uib-ws.md)

[Report an issue](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/report-grc-issue-frm-plan.md)

