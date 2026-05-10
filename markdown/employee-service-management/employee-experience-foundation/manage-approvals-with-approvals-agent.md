---
title: Manage approvals with Now Assist Approval Assistance AI agent
description: Manage the approvals that are assigned to you by using the Now Assist Approval Assistance Agent for REQ and RITM.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use, Now Assist for Employee Experience, Unified Employee Experience, Employee Service Management]
---

# Manage approvals with Now Assist Approval Assistance AI agent

Manage the approvals that are assigned to you by using the Now Assist **Approval Assistance Agent** for REQ and RITM.

## Before you begin

Ensure that you

-   Download the Now Assist for Employee Experience plugin.
-   Learn about AI agents and have read access to the record to auto-process approvals.
-   Ensure you are on Zurich patch 4 or above.
-   The agent supports only REQ and RITM.

Role required: approver\_user, sn\_request\_read, sn\_write

## About this task

Use the Now Assist Approval Assistance Agent to manage your assigned approvals. Using an AI agent, you can

-   Pull all the information and records for approvals automatically.
-   Review the policies, checklist, and evaluation criteria.
-   Approve the requests based on the Now Assist recommended decision.

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Employee Center** &gt; **My tasks**.

2.  Select the request from the available list that you want to work on.

    The details are displayed on the card with the summary.

3.  Select the **Review with NowAssist** button.

    NowAssist performs the following actions:

    -   Triggers an AI agent to review the request.
    -   Verifies the request for policy compliance.
    -   Generates an eligibility checklist and criteria.
    -   Shows the criteria for match or mismatch.
    -   Provides an option to act on approval such as **Approve** and **Reject**

        **Note:** You can select **View AI Agent Processing Steps** to see the details.

    ![Approval Assitance agent checklist](../images/na-agent-review-rules.png "Review with NowAssist")

4.  Select **Approve** or **Reject**.

    ![Summarization on NowAssist for Employee Experience on click](../images/na-agent-review-action.png "Approve or reject with NowAssist")

    **Note:** Currently, HR requests aren't supported out-of-the-box.

    The response appears `I am ready to process your approval request for <request description>. Is it okay to proceed?`

5.  Select **Yes** or **No**.

    ![Summarization on NowAssist for Employee Experience on click](../images/na-agent-review-action.png "Confirm Approval with NowAssist")

    **Note:** The agent supports only REQ and RITM. HR requests aren’t supported. However, by configuring the `sp_approval_configuration` record, you can set up support for for HR case too.

6.  Request is approved and moved from **Open** to the **Completed** tab.


## What to do next

Review how to set up and use the Approval Assistance AI agent. For more information about agentic workflow and activating the required components, see the following topics:

-   [Platform Approval assistance AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-approval-aia.md)
-   [Activate an agentic workflow template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/activate-aia-use-case.md)
-   [Modify an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/modify-ai-agent.md)
-   [Implement access control in Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-security-implementation.md)

There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see [Find AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/find-ai-agents.md).

**Parent Topic:**[Using Now Assist for Employee Experience](../concept/use-now-assist-for-emp-exp.md)

**Related topics**  


[Check your to-do tasks by using the Now Assist in Virtual Agent](check-todo-tasks-using-the-now-assist-virtual-agent.md)

[Check your approvals by using Now Assist in Virtual Agent](check-your-approvals-using-now-assist-virtual-agent-emp-exp.md)

[Check company news and events](check-company-news-using-nowassist-va.md)

[View summarization for approvals](view-summarization-approvals.md)

