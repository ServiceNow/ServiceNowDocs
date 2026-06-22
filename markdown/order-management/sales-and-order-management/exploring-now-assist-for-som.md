---
title: Exploring Now Assist for SFA
description: With the Now Assist for Sales Force Automation \(SFA\) application, sales agents can manage the lifecycle of leads by automating outreach, follow-up communications, demo bookings, and handling lead disinterest or opt-outs. It can operate independently or under human supervision, thereby streamlining engagement and demo scheduling.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/sales-and-order-management/exploring-now-assist-for-som.html
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-06-09"
reading_time_minutes: 3
breadcrumb: [Now Assist for SFA, Sales Customer Relationship Management]
---

# Exploring Now Assist for SFA

With the Now Assist for Sales Force Automation \(SFA\) application, sales agents can manage the lifecycle of leads by automating outreach, follow-up communications, demo bookings, and handling lead disinterest or opt-outs. It can operate independently or under human supervision, thereby streamlining engagement and demo scheduling.

## Now Assist for Sales Force Automation \(SFA\) overview

Sales agents use the Now Assist for Sales Force Automation \(SFA\) AI agent collection to complete these tasks autonomously:

1.  Follow-up/Nudge Emails: Automated follow-ups at defined intervals if leads do not respond, with escalation to sales agents for disqualification.
2.  Demo Booking/Rebooking/Cancellation: Reviews lead email replies to book, reschedule, or cancel demos, checking sales agent calendars and sending confirmations.
3.  Lead Disinterest/Opt-Outs: Identifies disinterest or opt-out requests from emails, updating lead status and ensuring compliance \(for example, unsubscribe links\).

## Now Assist for Sales Force Automation \(SFA\) users

|User|Description|
|----|-----------|
|Sales Manager/Admin|Configure the AI agents.|
|Sales Agent|Access to Now Assist Panel.|

## Now Assist for Sales Force Automation \(SFA\) benefits

-   Accelerates sales and order processing.
-   Improves accuracy and reduces operational risk.
-   Enhances user productivity with intuitive AI support.

## Now Assist for Sales Force Automation \(SFA\) skills

The Now Assist for Sales Force Automation \(SFA\) application includes the generative AI skill that produces concise, structured summaries of opportunities in the CRM Workspace. The opportunity summarization provides sales representatives and managers an immediate view of key details without reviewing multiple records.

The opportunity summary draws from the following related tables by default:

-   Opportunity and opportunity line items
-   Activity data: touchpoints, appointments, meetings, emails, work notes, and tasks
-   Opportunity competitors and contacts
-   Account or consumer table

The opportunity summary appears on the Overview page and includes the following sections:

-   **Opportunity overview**

    Key details including the short description, opportunity amount, stage, account name, and the top three line items by value. For closed opportunities, the summary includes the outcome: won opportunities show the signed date; lost opportunities show the lost reason, competitor, and close date.

-   **Customer needs and pain points**

    The top two customer needs or pain points identified from the opportunity description, business goals and pain points from emails, and work notes. When sources conflict, the most recent email or work note takes precedence. The source of each need or pain point is included in the summary.

-   **Recent and upcoming activity**

    The most recent activity from touchpoints or emails, with its date and a brief description. Also includes the next open task with its due date, or the next scheduled touchpoint or meeting.

-   **Risks detected from activity**

    Up to two risks identified from recent emails, meetings, touchpoints, and tasks. Each risk includes the source. Risk types include unresolved technical concerns, budget uncertainty, timeline pressure, competitor activity, negative sentiment, price objections, and reduced scope.


## CRM conversational query

CRM conversational query is an AI agent embedded in the Now Assist panel. You can ask questions and issue commands in plain language and the agent performs the action without you opening a form.

The agent is accessible via MCP clients \(such as Claude\) through the Sales CRM MCP server, which is published in Sales common. For information on how to connect to an MCP server from an MCP client, refer [Connecting to an MCP server from an MCP client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/connect-mcp-server-client.md).

The agent supports the following operations on opportunity records and related entities, including contacts, tasks, touchpoints, meetings, line items, and competitors:

-   **Retrieve**: view pipeline snapshots, opportunity details, tasks, touchpoints, contacts, accounts, and opportunity lines.
-   **Update**: change field values on opportunities and related records. Multi-field updates \(up to five fields in one prompt\) and relative date expressions such as "end of next month" are supported.
-   **Create**: add opportunities, contacts, tasks, touchpoints, and competitors.
-   **Delete**: remove junction or child records such as opportunity competitors and associated contacts. Parent records such as the opportunity itself, the contact record, or the product are never deleted.

## What to explore next

To learn more about configuring and using Now Assist for Sales Force Automation \(SFA\), see:

-   [Configure Now Assist for Sales Force Automation \(SFA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-and-order-management/configure-now-assist-som.md)
-   [Use agentic workflows in Now Assist for Sales Force Automation \(SFA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-and-order-management/using-agentic-worklflows-in-lead-management.md)

