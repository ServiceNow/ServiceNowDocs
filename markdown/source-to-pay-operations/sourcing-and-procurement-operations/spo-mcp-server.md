---
title: SPO MCP Server
description: Use the SPO Model Context Protocol \(MCP\) Server to complete sourcing and procurement tasks in conversational interfaces such as Claude and Moveworks, without accessing the ServiceNow instance directly.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/spo-mcp-server.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-08-25"
reading_time_minutes: 1
breadcrumb: [ServiceNow Otto for SPO, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# SPO MCP Server

Use the SPO Model Context Protocol \(MCP\) Server to complete sourcing and procurement tasks in conversational interfaces such as Claude and Moveworks, without accessing the ServiceNow instance directly.

The SPO MCP Server connects procurement operations to the MCP client applications in your organization. Submit purchase requests, track request status, complete approvals, and receive notifications about your procurement activity without leaving your MCP client.

## Supported MCP clients

The SPO MCP Server supports any MCP-compatible client application, including:

-   Claude \(Claude.ai web and mobile\)
-   Moveworks

## Key capabilities

The SPO MCP Server provides the following capabilities:

-   **Conversational intake**

    Intelligent workflow that answers procurement questions, asks discovery questions to validate selections against KB articles and approval rules, then routes to pre-filled on-catalog or off-catalog request forms.

-   **Status visibility**

    Requesters can search for and track their sourcing, procurement, and purchase order records, view details, related tasks, and comments, and add records to a watchlist.

-   **Task completion**

    Users complete approval, sourcing, and acknowledgement tasks directly in chat. Tasks that require external interactions such as video calls or document signing, route to Employee Center.

-   **Proactive notifications**

    Users receive targeted notifications when requests are created, tasks are assigned, approvals are completed, or requests are rejected. Users can take action or route to external workflows from the notification.


## SPO MCP Server users

|Users|Responsibilities|
|-----|----------------|
|Administrators|Configure the SPO MCP Server in your ServiceNow instance.|
|Employees and requesters|Submit purchase requests and track request status through an MCP client application without accessing the ServiceNow instance.|

## How the SPO MCP Server works

The SPO MCP Server operates as a secure intermediary between any MCP client application and the ServiceNow instance:

1.  The SPO MCP Server user asks a question using an MCP client. For example, an employee or requester opens an MCP client such as Moveworks or Claude and asks a question about a procurement request.
2.  The MCP client sends the question to the SPO MCP Server using the Model Context Protocol.
3.  The SPO MCP Server authenticates the user against the ServiceNow role-based access control.
4.  The SPO MCP Server retrieves the requested data or performs the requested action in the ServiceNow instance.
5.  The SPO MCP Server returns the result to the MCP client, which displays the result to the user.

