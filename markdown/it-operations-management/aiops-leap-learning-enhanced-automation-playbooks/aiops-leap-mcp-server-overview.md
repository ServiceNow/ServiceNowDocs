---
title: LEAP MCP Server
description: External AI clients can query LEAP automation data using Model Context Protocol \(MCP\) tools exposed through the ITOM MCP Server.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/aiops-leap-mcp-server-overview.html
release: australia
product: AIOps LEAP \(Learning-Enhanced Automation Playbooks\)
classification: aiops-leap-learning-enhanced-automation-playbooks
topic_type: concept
last_updated: "2026-08-13"
reading_time_minutes: 3
keywords: [MCP, Model Context Protocol, external AI client, LEAP MCP tools, AIOps MCP Server]
breadcrumb: [Explore, Learning Enhanced Automation Platform \(LEAP\), ITOM Visibility, IT Operations Management]
---

# LEAP MCP Server

External AI clients can query LEAP automation data using Model Context Protocol \(MCP\) tools exposed through the ITOM MCP Server.

## Overview of LEAP with MCP

LEAP exposes automation capabilities as MCP tools within the ITOM AIOps MCP Server. External AI clients such as Claude, ChatGPT, Copilot, and Gemini can invoke these tools using the Model Context Protocol \(MCP\), a standardized protocol for AI client integration.

MCP tools provide a governed, product-supported path for connecting external AI clients to LEAP automation workflows. Without MCP tools, the integration path is a manual process with no authentication guardrails or ServiceNow support coverage.

All MCP tool invocations use OAuth 2.0 authentication. Access to specific tools is controlled by the LEAP AI SKU tier assigned to your instance.

## How MCP tools work

LEAP MCP tools are registered on the shared ITOM MCP Server \(`sn_genai.itom_mcp_server`\). When an external AI client connects to the server and calls `tools/list`, the LEAP tools appear alongside tools from other ITOM products. The server URL takes the form:`https://<instance>.service-now.com/sncapps/mcp-server/mcp/sn_genai_itom_mcp_server`

**Warning:** LEAP specific MCP tool invocations require the sn\_itom\_leap.leap\_viewer role at minimum. Other tools on the ITOM MCP Server might still work, but LEAP specific tools fail with an unauthorized error if the user lacks this role: `User is missing required role: sn_itom_leap.leap_viewer`.

The following describes the invocation flow:

1.  The external AI client authenticates to the ITOM MCP Server using an OAuth 2.0 token.
2.  The client calls a LEAP MCP tool with the required input parameters.
3.  The MCP Server routes the request to the underlying LEAP API.
4.  The server returns a structured JSON response to the client.

## Tool categories

LEAP MCP tools are registered as **Action** tools on the ITOM MCP Server and are organized into three categories:

|Tools|Description|
|-----|-----------|
|LEAP - Get App setup status|Reports LEAP setup and grouping pipeline readiness. Use this tool to check whether LEAP is configured before invoking automation opportunity tools. For example, if an AO query returns no data, `get_app_setup_status` can confirm whether setup is incomplete and return the URL of the setup page.|
|LEAP - Get property or setting|Retrieves specific LEAP configuration properties by key. Only properties on an explicit allow-list are accessible. For example, retrieve `missed_opportunity_threshold` \(the number of missed opportunities above which an AO is flagged as high priority\) or `default_resolution_steps_filter` \(the encoded query that controls which AOs receive AI-generated resolution steps\).|
|LEAP - Get automation opportunities|Provides read-only access to automation opportunity data. External clients can query for lists of AOs, retrieve full details for a specific AO, and filter results by keyword, status, or linked artifacts. For example, an AI client can ask for all AOs related to Discovery issues that have a KB article generated, or retrieve details for a specific AO number such as AOPP0000173.|

## Set up the MCP connection

To connect an external AI client to LEAP MCP tools, you must configure OAuth authentication on the ITOM MCP Server. A banner on the MCP Server Console confirms when OAuth setup is required. For setup instructions, see [Activate the ITOM MCP Server Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/activate-itom-mcp-server.md).

## What to explore next

-   [Exploring LEAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/exploring-aiops-leap.md)
-   [Automation opportunities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/automation-opportunities.md)

