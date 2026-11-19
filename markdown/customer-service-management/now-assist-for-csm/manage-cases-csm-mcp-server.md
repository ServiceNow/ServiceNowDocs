---
title: Manage cases using the CSM MCP Server
description: Use the CSM MCP Server to retrieve lists of cases and case tasks and view details for specific cases and case tasks through an MCP client application such as Moveworks or Claude on the web.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/customer-service-management/now-assist-for-csm/manage-cases-csm-mcp-server.html
release: australia
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2026-08-24"
reading_time_minutes: 1
keywords: [CSM MCP Server, case management, MCP client, customer service cases]
breadcrumb: [Set up the CSM MCP Server, CSM MCP Server, ServiceNow Otto for CSM, Customer Service Management]
---

# Manage cases using the CSM MCP Server

Use the CSM MCP Server to retrieve lists of cases and case tasks and view details for specific cases and case tasks through an MCP client application such as Moveworks or Claude on the web.

## Before you begin

Your system administrator configures the integration between your MCP client application and your instance during setup.

Role required:

|Tool|Role|Purpose|
|----|----|-------|
|get\_customer\_service\_cases|sn\_csm\_mcp\_invoke|Required to invoke get\_customer\_service\_cases tool|
|get\_case\_tasks|sn\_csm\_mcp\_invoke|Required to invoke get\_case\_tasks tool|

## About this task

The CSM MCP Server uses two tools to handle case management. The MCP client application automatically selects the appropriate tool based on your prompt.

For information on tools, see [CSM MCP Server tools reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/now-assist-for-csm/csm-mcp-server-tools-reference.md).

## Procedure

1.  Open your MCP client application such as Moveworks or Claude on the web that is connected to your ServiceNow instance using the CSM CSM MCP Server.

    Your system administrator configures this integration during setup.

2.  Enter a prompt to query or retrieve a list of cases and case tasks.

    The following examples show prompts for each tool:

    -   **get\_customer\_service\_cases:** Retrieves a list of cases for given criteria or details of a specific case.

        Example prompts:

        -   "Give me list of cases opened today"
        -   "Give me list of open cases by priority for account Boxeo"
        -   "Give me list of open priority cases missing SLA"
        -   "What is this case?"
        **Note:** This tool is read-only.

    -   **get\_case\_tasks:** Retrieves a list of case tasks for given criteria or details of specific case tasks.

        Example prompts:

        -   "Tell me about the case tasks in CS0001183."
        -   "Verify legal business registration documents for CS0001183"
        **Note:** This tool is read-only.

3.  Review the MCP client application response.

    The MCP client application retrieves data from your ServiceNow instance and presents it in the chat. The response includes only data you have permission to access.


