---
title: Manage tasks and approvals
description: Triage your queue from the EmployeeWorks Web App Tasks and requests. Review task summaries, act on approvals, apply conversational filters, and retrieve items through chat.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/employee-experience-foundation/eslate-work-with-inbox.html
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-05-28"
reading_time_minutes: 2
keywords: [employee communications, announcements, content library, employee slate, chat promotion]
breadcrumb: [Tasks and requests, Working with EmployeeWorks capabilities, ServiceNow EmployeeWorks Web App, Unified Employee Experience, Employee Service Management]
---

# Manage tasks and approvals

Triage your queue from the EmployeeWorks Web App Tasks and requests. Review task summaries, act on approvals, apply conversational filters, and retrieve items through chat.

## Before you begin

Verify the Now Assist is active on the instance. AI summaries, AI prioritization, conversational filters, and chat-driven approval actions require Now Assist.

Role required: Employees

## About this task

You can view, track, and act on pending tasks, approvals, and open requests across enterprise systems. These systems include HR approvals, IT tasks, learning content, and surveys.

## Procedure

1.  Open **Tasks and requests** in one of the following ways.

    -   Select the **Tasks and requests** widget on the home page.
    -   Select **Tasks and requests** in the side navigation.
2.  Review items in the **Tasks** and **Requests** tabs.

    The **Tasks** tab lists tasks and approvals assigned to you, sorted by AI prioritization. The **Requests** tab lists requests that you or others created for you. Each card shows an AI-generated summary of who is asking, what is needed, and why it matters. Select **Sort by created date**to order the list by creation date instead. For more information, see [Configure tasks and requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/emp-slate-tasks-requests.md).

3.  Open a card to view the task detail and approval checklist.

    The administrator can select **Link to task** in the task configuration. When enabled, opening the card redirects to the parent record instead of the task detail page. Parent records include HR cases and requested items.

    The task detail includes a summary of the request and a checklist that highlights which knowledge article conditions the request meets.

4.  Review the summaries and insights based on the skill configuration and the mode.

    For more information on building a custom skill, see [Configure a custom AI insights skill for a task type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/empworks-configure-ai-insights-skill.md).

5.  Apply a conversational filter.

    Ask the chat to filter, for example by overdue status or by request type. Ask the chat to clear filters to return the full list. Conversational filters are additive to the filter configuration that the administrator sets.

6.  Retrieve tasks or requests through chat.

    Ask the chat for your tasks or requests to receive a task or request widget that lists matching items. Select **View details** in the widget to open the task detail without leaving the conversation.

7.  Track a specific incident, case, or request through chat.

    Ask the chat about a specific record, for example an incident number. The chat returns a single-item widget that you use to review and act on the record.

8.  Perform the actions such as **Approve** or **Reject** the item.

    Take action from the detail page or enter a natural language command in chat such as `Approve this request` or `Reject this request`.

    The system updates the record state based on your action.


**Related topics**  


[EmployeeWorks Web App prompt library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/employee-slate-prompt-library.md)

