---
title: Using Interview Management
description: You can schedule and document interviews and use interview templates using the Core UI or HR Service Delivery Agent Workspace.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using HR Service Delivery Employee Relations, Employee Relations, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Using Interview Management

You can schedule and document interviews and use interview templates using the Core UI or HR Service Delivery Agent Workspace.

Creating a record of an interview is an important part of an employee relations investigation.

Scheduling an interview: There are two \(2\) methods you can use to schedule an interview:

-   Manual entry: You enter a start and end date/time for the interview and confirm outside the application.

    **Note:** In legacy UI, the manual entry is the only method available for scheduling an interview.

-   Use Microsoft Outlook Calendar to schedule an interview.

    -   To use this feature, you must integrate with Microsoft Exchange. Ensure the **sn\_hr\_er.ex\_online\_notification\_url** system property contains the Callback URL in the **Value** field. For more information, see [Set up Microsoft Exchange Online spoke](https://www.servicenow.com/docs/access?context=setup-ms-exch-ol&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).
    -   The **sn\_hr\_er.exchange\_online\_max\_candidate** system property determines the maximum number of meeting time slots to return when trying to schedule an interview using Microsoft Exchange. The default value is 500 slots.
    **Note:** You can use the manual method of scheduling in HR Service Delivery Agent Workspace. For more information, see [Schedule an interview in Employee Relations using the legacy UI](../task/hr-er-interview.md) or [Schedule an interview in Employee Relations using Agent Workspace for HR Case Management](../task/hr-er-interview-ws.md).


