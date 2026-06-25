---
title: Tasks and requests
description: Tasks and requests provides a unified interface for managing tasks, approvals, and action items.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/employee-experience-foundation/emp-slate-inbox.html
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2026-04-02"
reading_time_minutes: 2
keywords: [Tasks and requests, tasks, approvals, requests, Employee Slate]
breadcrumb: [Working with Employee Slate capabilities, Employee Slate, Unified Employee Experience, Employee Service Management]
---

# Tasks and requests

Tasks and requests provides a unified interface for managing tasks, approvals, and action items.

The **Tasks and requests** \(formerly known as Inbox\) replaces the fragmented experience of managing work across multiple queues and modules. All tasks, approvals, and active requests assigned to an employee appear in a single consolidated view.

## Tasks and requests contents and configuration

The tasks and requests section aggregates the following work item types:

-   Tasks assigned to the employee.
-   Active service requests that the employee submitted.

You can use the filters to view and track the tasks and requests from the following sources:

-   To-Do configurations for task items.
-   My Request Filter configurations for request items.

## Tasks and requests pages

Employee Slate provides task and request detail pages with all the context that an employee needs. Task and request types natively render with the full AI-native experience with AI Insights for approvals. For other types, the tasks and requests provides a link to Employee Center.

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

Access all your tasks, approvals, and requests from a unified space Employee Slate. You can view, track, and act on pending tasks, approvals, and open requests across enterprise systems. These systems include HR approvals, IT tasks, learning content, and surveys.

-   Apply a filter by asking the chat to narrow the items, for example by overdue status or by request type.
-   Clear filters by asking the chat to reset the view.
-   Approve or reject an approval from the details page with prompts and chat.
-   Filter tasks by state, for example, select **Completed** to view all completed tasks.
-   Ask about a specific incident, case, or request to track and take action from chat.

Conversational filters apply along with the filters that administrators configure.

**Note:** AI summaries, AI prioritization, AI Insights for approvals, and chat-driven actions require Now Assist. Employee Slate deployments that use Moveworks without Now Assist include the tasks and requests without some AI capabilities.

**Related topics**  


[Employee Slate prompt library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/employee-slate-prompt-library.md)

