---
title: Inbox
description: The inbox provides a unified interface for managing tasks, approvals, and action items.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-02"
reading_time_minutes: 2
breadcrumb: [Working with Employee Slate capabilities, Employee Slate, Employee Service Management]
---

# Inbox

The inbox provides a unified interface for managing tasks, approvals, and action items.

The inbox replaces the fragmented experience of managing work across multiple queues and modules. All tasks, approvals, and active requests assigned to an employee appear in a single consolidated view.

## Inbox contents and configuration

The inbox aggregates the following work item types:

![Inbox items](../images/es-inbox.png "Inbox")

-   Tasks assigned to the employee.
-   Active service requests that the employee submitted.

You can use the filters to view and track the tasks and requests from the following sources:

-   To-Do configurations for task items.
-   My Request Filter configurations for request items.

## Tasks and requests pages

Employee Slate provides task and request detail pages with all the context that an employee needs.

Task and request types natively designed for the inbox render with the full AI-native experience, including AI Insights for approvals. For other types, the inbox provides a link to Employee Center.

## AI prioritization and summaries

With Now Assist, each task card in the To-dos tab includes an AI-generated summary. The summary covers the following information:

-   Who is asking
-   What is needed
-   Why it matters

By default, the To-dos list sorts by AI prioritization. Items that need immediate action appear first. The following details describe how prioritization works:

-   The assistant evaluates urgency, due dates, business impact, and dependencies to rank items.
-   Consumption details are available in the `sn_ex_ai_portal_to_do_activities` table with scores for each task.
-   The daily execution cap is defined in the `smartpriority_daily_assist_consumption_limit` system property.
-   Logs are available in the `sys_generative_ai_log_list` table. Search by the skill name to view the reasoning behind a particular task score.

**Note:** When you exhaust the daily execution cap, the skill stops running for the rest of the day. The default is 3,000 executions per day. Administrators can increase the consumption limit based on usage.

## AI Insights for approvals

For approval items, Now Assist analyzes the approval request. It surfaces a checklist of the conditions that apply to the decision. The insights highlight:

-   Conditions that the request meets based on associated knowledge articles and policies such as keyword, body text, short description, or meta description.
-   Conditions that the request doesn't meet or that need review.

AI-generated insights may not reflect every relevant policy condition. Verify AI-generated insights against authoritative policy sources before making approval decisions.

## Conversational filters and chat-driven actions

The inbox is a single place for tasks, approvals, and requests in Employee Slate. You can view, track, and act on pending tasks, approvals, and open requests across enterprise systems. These systems include HR approvals, IT tasks, learning content, and surveys.

![chat about inbox items](../images/es-inbox-chat.png "Inbox chat")

Employees interact with the inbox through natural language in the chat panel:

-   Apply a filter by asking the chat to narrow the inbox, for example by overdue status or by request type.
-   Clear filters by asking the chat to reset the view.
-   Approve or reject an approval from the details page with prompts and chat.
-   Filter tasks by state, for example, select **Completed** to view all completed tasks.
-   Ask about a specific incident, case, or request to track and take action from chat.

Conversational filters apply in addition to the inbox filters that administrators configure.

**Note:** AI summaries, AI prioritization, AI Insights for approvals, and chat-driven inbox actions require Now Assist. Employee Slate deployments that use Moveworks without Now Assist include the inbox, but not these AI capabilities.

**Related topics**  


[Employee Slate prompt library](../reference/employee-slate-prompt-library.md)

