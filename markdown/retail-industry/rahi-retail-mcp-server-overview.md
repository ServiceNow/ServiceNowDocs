---
title: Retail MCP Server
description: The Retail MCP Server exposes Retail Service Management capabilities as Model Context Protocol \(MCP\) tools, so store staff can find their store and devices and raise, track, and update Store Services cases from their AI assistant.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/rahi-retail-mcp-server-overview.html
release: brazil
topic_type: concept
last_updated: "2026-09-23"
reading_time_minutes: 4
keywords: [Retail MCP Server, MCP, Model Context Protocol, AI assistant, break-fix, store inquiry]
breadcrumb: [ServiceNow Otto for Retail Service Management \(RSM\), Retail]
---

# Retail MCP Server

The Retail MCP Server exposes Retail Service Management capabilities as Model Context Protocol \(MCP\) tools, so store staff can find their store and devices and raise, track, and update Store Services cases from their AI assistant.

Without the Retail MCP Server, a store associate who uses an AI assistant has to leave the conversation and open the portal to find their store, check on a case, or report broken equipment. The Retail MCP Server lets the assistant do this work on the associate's behalf, using the associate's own identity and access rights.

## One server for all retail tools

The application registers a single MCP server, **Retail MCP Server**. MCP-compatible AI clients, such as ServiceNow Otto, Now Assist, and Claude, discover and connect to this one server. Every retail tool registers under it, so new retail capabilities become available to the assistant without a new server being set up.

## Available tools

The Retail MCP Server provides six tools. The assistant usually chains them: it identifies the store first, then the device, and then the case.

-   **Get my retail store**

    Returns the stores the signed-in user belongs to.

-   **Get store devices**

    Returns the devices registered to a store, so the assistant can match "the freezer in aisle 3" to a real device.

-   **Create store break-fix case**

    Reports a broken or faulty device to HQ.

-   **Create store inquiry case**

    Sends HQ a question about store policy, process, or operations.

-   **Get my store services cases**

    Lists the break-fix and store inquiry cases the user raised.

-   **Update store services case**

    Comments on, accepts or rejects a proposed resolution for, or closes one of the user's cases.


The four case tools install only when the Retail Store Services plugin is active. The store and device tools work without it.

## Access and identity

Each tool runs as the calling user. The tools identify the user from the authenticated session, never from a user name or ID that the assistant supplies, and they return only records that the user can already read in the platform. Each tool also requires a specific role before it can be invoked. For details, see [Retail MCP Server roles and data access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-mcp-server-access-control.md).

## What the Retail MCP Server doesn't do

-   It provides no user interface. Store staff work entirely in their AI assistant.
-   It doesn't create, update, or delete devices. Device access is read-only.
-   It supports only break-fix and store inquiry cases.
-   It doesn't let callers change a case's state directly, or its priority, assignment, or resolution code. Callers can only comment, respond to a proposed resolution, or close the case.
-   It doesn't choose a primary store for a user who belongs to several stores. The assistant asks the user which store to use.

-   **[Set up the Retail MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-mcp-server-set-up.md)**  
Install the Retail MCP Server, connect your AI client to it, and give store staff the roles they need, so they can work with Retail Service Management from their AI assistant.
-   **[Report a broken device from your AI assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-report-device-issue-ai-assistant.md)**  
Create a break-fix case for broken or faulty equipment in your store by describing the problem to your AI assistant, without opening the portal.
-   **[Ask HQ a question from your AI assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-ask-hq-question-ai-assistant.md)**  
Get an official answer from HQ about store policy, process, or operations by raising a store inquiry case from your AI assistant.
-   **[Track and update your cases from your AI assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-track-update-case-ai-assistant.md)**  
Check the status of your break-fix and store inquiry cases, answer questions from HQ, respond to proposed resolutions, and close cases, all from your AI assistant.
-   **[Retail MCP Server tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-mcp-server-tools.md)**  
The Retail MCP Server provides six tools. Each entry lists the tool's purpose, inputs, what it returns, whether it changes data, and what it requires.
-   **[Retail MCP Server roles and data access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-mcp-server-access-control.md)**  
Access to the Retail MCP Server is controlled at two levels: roles determine who can invoke each tool, and the caller's own record access determines what data each tool returns or changes.

**Related topics**  


[Set up the Retail MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-mcp-server-set-up.md)

[Retail MCP Server tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-mcp-server-tools.md)

[Retail MCP Server roles and data access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-mcp-server-access-control.md)

[ServiceNow Otto for Break-Fix and Store Audit overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/moveworks-breakfix-storeaudit-overview.md)

[Components Moveworks Integration for Break-Fix and Store Audit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/moveworks-breakfix-storeaudit-reference.md)

