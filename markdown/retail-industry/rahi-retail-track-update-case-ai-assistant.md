---
title: Track and update your cases from your AI assistant
description: Check the status of your break-fix and store inquiry cases, answer questions from HQ, respond to proposed resolutions, and close cases, all from your AI assistant.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/retail-industry/rahi-retail-track-update-case-ai-assistant.html
release: australia
topic_type: task
last_updated: "2026-09-23"
reading_time_minutes: 2
keywords: [break-fix, store inquiry, AI assistant, accept resolution, reject resolution]
breadcrumb: [Retail MCP Server, Configure, Retail]
---

# Track and update your cases from your AI assistant

Check the status of your break-fix and store inquiry cases, answer questions from HQ, respond to proposed resolutions, and close cases, all from your AI assistant.

## Before you begin

Your AI assistant must be connected to the Retail MCP Server. You can track and update only cases that you raised.

Role required: sn\_rtl\_stre\_servcs.contributor

## About this task

By default, the assistant shows only your open cases. Ask for your closed cases or case history if you need them. What you can do with a case depends on its state, and the assistant offers only the actions that are currently allowed.

## Procedure

1.  Ask the assistant about your cases.

    For example, "Show me my open cases," "Did HQ reply?", or "What's the status of RBF0001234?"

2.  If the assistant asks, tell it which case you mean.

3.  Review the case details and the actions that the assistant offers, and tell it what to do.

    -   To add information, tell the assistant what to add. It's added to the case as a comment.
    -   If the case is Awaiting Info, HQ has asked you a question. The assistant shows you the question. Give your answer, and the assistant adds it as a comment and the case moves back to Open.
    -   If the case is Resolved, HQ has proposed a resolution. The assistant shows it to you. Accept it to close the case, or reject it and give a reason to reopen the case.
    -   If you no longer need the case, ask the assistant to close it. You can close a case that's New, Open, or Awaiting Info.
4.  If the assistant asks you to confirm the action, confirm it.


## Result

The case is updated, and the assistant confirms the outcome and shows the case's current state. If the action isn't allowed, or the case doesn't exist or isn't yours, the assistant tells you, and the case isn't changed.

## What to do next

You can't change a case that's Closed or Cancelled. You also can't change a case's priority or assignment from the assistant.

**Parent Topic:**[Retail MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/retail-industry/rahi-retail-mcp-server-overview.md)

**Related topics**  


[Retail MCP Server roles and data access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/retail-industry/rahi-retail-mcp-server-access-control.md)

[Respond to resolutions through Portal or Mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/retail-industry/breakfix-respond-resolution.md)

[moveworks-breakfix-case-operations]

