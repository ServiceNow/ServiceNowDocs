---
title: Alert remediation with an MCP Client
description: Get remediation suggestions for an alert from an AI agent or MCP Client, matching what's available in Service Operations Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/itom-mcp-server-alert-remediation.html
release: australia
topic_type: concept
last_updated: "2026-07-09"
reading_time_minutes: 2
breadcrumb: [Use the ITOM MCP Server Console, AI in ITOM, IT Operations Management]
---

# Alert remediation with an MCP Client

Get remediation suggestions for an alert from an AI agent or MCP Client, matching what's available in Service Operations Workspace.

## Alert remediation tool overview

MCP tools retrieve data from your ServiceNow instance and perform alert actions.

The Alert remediation tool lets you request a remediation suggestion for an alert through natural-language prompts in your MCP Client, without switching to the ServiceNow UI. The tool routes your request to the existing remediation agent that already runs in Service Operations Workspace, so you get the same suggestion regardless of channel.

**Important:**

The Alert remediation tool suggests actions through an AI agent or MCP Client. You're interacting with AI. AI-generated responses may be inaccurate or incomplete. Review the suggestion and the linked alert before taking action.

## Supported capabilities

The Alert remediation tool supports the following capabilities:

-   Accepts a request for a specified alert and returns a remediation suggestion based on existing workflows, knowledge base articles, and related context.
-   Returns the remediation recommendation directly in the response and prompts you to execute or dismiss it.
-   Lets you execute the suggested remediation directly through the MCP Client.
-   If a remediation fails to execute, the tool offers a fallback action, such as creating an incident, and requests confirmation before running it.

## Considerations

Consider the following when using the Alert remediation tool:

-   Initial availability may cover only a subset of alert types or remediation actions.
-   Remediation suggestions are scoped to the alerts you're authorized to view.

## Use cases

The Alert remediation tool is useful in the following scenarios:

-   An operator asks their MCP Client, such as AWS Claude, "What should I do about this alert?" and receives a remediation suggestion grounded in existing workflows and knowledge base articles.
-   An operator working from an external AI agent reviews a suggested remediation and confirms before executing it.

## Workflow

The Alert remediation tool operates as part of the ITOM MCP Server Console workflow:

1.  An operator asks the external agent what to do about a specified alert.
2.  The MCP Client sends the request to the ITOM MCP Server Console using the Model Context Protocol \(MCP\).
3.  The ITOM MCP Server Console authenticates the request against ServiceNow role-based access control.
4.  The request is routed to the existing remediation agent, which evaluates the alert against workflows, knowledge base articles, and related context.
5.  The ITOM MCP Server Console returns the remediation recommendation to the MCP Client, which prompts the operator to execute or dismiss it.

**Related topics**  


[Use the ITOM MCP Server Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/use-itom-mcp-server.md)

[Alert actions through an MCP Client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-mcp-server-alert-actions.md)

