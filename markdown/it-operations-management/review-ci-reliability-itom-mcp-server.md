---
title: Review CI reliability with an MCP Client
description: Use an MCP Client with the ITOM MCP Server Console to review configuration item \(CI\) reliability and topology, assess incident impact on reliability, and create service level objectives \(SLOs\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/review-ci-reliability-itom-mcp-server.html
release: australia
topic_type: task
last_updated: "2026-04-27"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [CI reliability and topology assessment, Use the ITOM MCP Server Console, AI in ITOM, IT Operations Management]
---

# Review CI reliability with an MCP Client

Use an MCP Client with the ITOM MCP Server Console to review configuration item \(CI\) reliability and topology, assess incident impact on reliability, and create service level objectives \(SLOs\).

## About this task

## Before you begin

Verify that the ITOM MCP Server Console is active and the required plugins are installed on your instance. For more information, see [Activate the ITOM MCP Server Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/activate-itom-mcp-server.md).

Role required: sn\_sow\_slo.slo\_operator

## Procedure

1.  Open your MCP Client application.

2.  In the MCP Client, ask a question or request an action for a CI.

    The following are common types of prompts:

    -   Review the reliability impact of an incident: "What is the reliability impact of incident INC0010217?"
    -   Review CI reliability status: "Show the reliability status of Customer Portal Service."
    -   Review CI reliability topology: "Show the reliability topology of Customer Portal Service. I want to understand whether other CIs are affected."
    -   Create an SLO for a CI: "Create an SLO for Auth Service."
3.  Review the MCP Client response.

    The MCP Client retrieves data from your ServiceNow instance and presents it in the chat. The response includes only data that you can access.


## What to do next

If you created an SLO, you can learn more about SLOs, including SLO types and compliance periods, in [Reliability metrics in SLO Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-level-objective-management/sr-work-SLI-SLO.md). To edit or deactivate an SLO, see [Edit a reliability metric](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-level-objective-management/sr-edit-sli-slo.md).

