---
title: Generate approval recommendations with generative AI
description: Use a generative AI skill to streamline the approval process for exceptions and false positive requests with AI-driven recommendations. Reduce manual effort and improve decision accuracy for your approvers in the Security Exposure Management Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/sem-approval-recommendation-skill.html
release: zurich
topic_type: task
last_updated: "2026-07-24"
reading_time_minutes: 1
breadcrumb: [Approval recommendations using generative AI, Use, Unified Security Exposure Management, Security Operations]
---

# Generate approval recommendations with generative AI

Use a generative AI skill to streamline the approval process for exceptions and false positive requests with AI-driven recommendations. Reduce manual effort and improve decision accuracy for your approvers in the Security Exposure Management Workspace.

## Before you begin

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see .

The ServiceNow Otto® panel must be activated. For more information, see [Activate the ServiceNow Otto panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/activate-now-assist-panel.md).

**Important:** This generative AI skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

Role required: sn\_sec\_exception.approver

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management** &gt; **List** &gt; **Approvals**.

2.  Select a request from the **All Approvals** list or from one of the widgets.

    **Note:** You can select any type of request except the requests related to exception rules.

3.  Select **Otto Recommendation** from the side panel to generate tailored recommendations for this request.

4.  Review the generated recommendations displayed in the **Otto Recommendation** panel.

5.  Select **Approve** or **Reject** at the top corner of the screen based on the tailored recommendations for this request.


## What to do next

-   **Refresh** the recommendation with the refresh icon. Refresh generates a fresh recommendation by analyzing latest data related to the request.
-   **Provide feedback** using the thumbs up/down icons to rate the usefulness of the recommendation.

**Parent Topic:**[Approval recommendations using generative AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/now-assist-vr-generating-approvals.md)

