---
title: Manage tasks and approvals
description: Triage your queue from the EmployeeWorks Web App Tasks and requests. Review task summaries, act on approvals, apply conversational filters, and retrieve items through chat.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/employee-experience-foundation/eslate-work-with-inbox.html
release: brazil
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-05-28"
reading_time_minutes: 3
keywords: [employee communications, announcements, content library, employee slate, chat promotion]
breadcrumb: [Tasks and requests, Working with EmployeeWorks capabilities, ServiceNow EmployeeWorks Web App, Unified Employee Experience, Employee Service Management]
---

# Manage tasks and approvals

Triage your queue from the EmployeeWorks Web App Tasks and requests. Review task summaries, act on approvals, apply conversational filters, and retrieve items through chat.

## Before you begin

Verify the Now Assist is active on the instance. AI summaries, AI prioritization, conversational filters, and chat-driven approval actions require Now Assist.

The Case and Knowledge Management for EmployeeWorks plugin extends HR task management capabilities to the AI-native EmployeeWorks experience. It Provides modern task interfaces for supported task types with integrated AI chat support for task assistance.

Role required: Employees

## About this task

You can view, track, and act on pending tasks, and approvals across enterprise systems.

## Procedure

1.  Open **Tasks and requests** in one of the following ways.

    -   Select the **Tasks and requests** widget on the home page.
    -   Select **Tasks and requests** in the side navigation.
2.  Review items in the **Tasks** and **Requests** tabs.

    The **Tasks** tab lists tasks and approvals assigned to you. Each card shows an AI-generated summary of who is asking, what is needed, and why it matters. Tasks are sorted by AI prioritization by default. You can sort by **Due date** or **Created date** instead.

    For more information, see [Configure tasks and requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/employee-experience-foundation/emp-slate-tasks-requests.md).

3.  Open a card to view task details and the approval checklist.

    The administrator can select **Link to task** in the task configuration. When enabled, opening the card redirects to the parent record instead of the task detail page. Parent records include HR cases and requested items.

    The following task types are displayed with modern task interfaces with integrated AI chat support for task assistance:

    -   Approval
    -   Checklist
    -   E-signature
    -   Schedule a meeting
    -   Mark When Complete
    -   Upload documents
    -   URL
    -   View video
    In the task interface, the Details tab shows the task summary, the Activity tab shows the activity log, and the Attachments tab shows related files.

    An optional approval checklist highlights which conditions the request meets.

    Complete and Skip buttons appear below. Chat context is preserved; any changes you make in chat automatically update the task record.

4.  Apply a conversational filter.

    Ask the chat to filter, for example by overdue status or by request type. Ask the chat to clear filters to return the full list. Conversational filters are additive to the filter configuration that the administrator sets.

5.  Retrieve tasks or requests through chat.

    Ask the chat for your tasks or requests to receive a task or request widget that lists matching items. Select **View details** in the widget to open the task detail without leaving the conversation.

6.  Track a specific incident, case, or request through chat.

    Ask the chat about a specific record, for example an incident number. The chat returns a single-item widget that you use to review and act on the record.

7.  Perform the actions such as **Approve** or **Reject** the item.

    Take action from the detail page or enter a natural language command in chat such as `Approve this request` or `Reject this request`.

    The system updates the record state based on your action.

8.  Access AI chat assistance for task guidance.

    Within a task detail, select **Can you help me?** to open the chat assistant. You can ask for help understanding the task, guidance on how to complete it, or clarification on what information is needed. The AI assistant reads the task context and provides relevant guidance specific to the task type.

    Chat context is preserved; any changes you make in chat automatically update the task record.

    Example requests: `Help me understand what this approval needs`, `What documents do I need to upload?`, or `How do I fill out this checklist?`

9.  Use **Mark as complete** or **Skip** buttons to update the task record.


**Related topics**  


[EmployeeWorks Web App prompt library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/employee-experience-foundation/employee-slate-prompt-library.md)

