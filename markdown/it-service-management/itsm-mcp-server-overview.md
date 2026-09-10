---
title: ITSM MCP Server
description: Connect an AI-enabled Model Context Protocol \(MCP\) client application to your ServiceNow environment using the ITSM MCP Server. This connection enables incident and change management for service desk agents and IT managers, and enables requesters to check and manage their own tickets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/itsm-mcp-server-overview.html
release: zurich
topic_type: concept
last_updated: "2026-07-07"
reading_time_minutes: 3
keywords: [ITSM MCP Server, Model Context Protocol, AI integration, incident management, change management, change requests, knowledge graph, Now Assist, service desk agents, IT managers, natural language, AI clients, Claude, Microsoft Copilot]
audience: [administrator, user]
breadcrumb: [IT Service Management]
---

# ITSM MCP Server

Connect an AI-enabled Model Context Protocol \(MCP\) client application to your ServiceNow environment using the ITSM MCP Server. This connection enables incident and change management for service desk agents and IT managers, and enables requesters to check and manage their own tickets.

## ITSM MCP Server capabilities

The ITSM MCP Server connects your ServiceNow ITSM environment to any AI-enabled MCP client, such as Moveworks or Claude. When agents ask questions about incidents or change requests, or requesters create or escalate tickets, the ITSM MCP Server retrieves data from the ServiceNow ITSM environment. It then performs actions for the agent through natural language conversation.

The ITSM MCP Server handles these core incident management capabilities:

-   Retrieves incident details based on the incident number.
-   Modifies incident details based on the incident number.
-   Retrieves incident assignees and assignment groups.
-   Searches and retrieves similar records.
-   Queries the ServiceNow Knowledge Graph to answer natural language questions about incident or change-related data.
-   Searches similar Knowledge Base \(KB\) articles based on the input query or incident details.
-   Retrieves details for a single published KB article.
-   Links a KB article to an incident as a related reference.

The ITSM MCP Server handles these core change management capabilities:

-   Answers natural-language questions about changes and related data across multiple tables.
-   Searches and retrieves change request data, similar changes, and aggregation of changes by various criteria for example, state, risk, or assignment group.
-   Executes the end-to-end change lifecycle, including creation, updates, and closure.
    -   Suggests the appropriate change model or template.
    -   Fills out change details such as assignment group, CIs, and planning fields.
    -   Steps through state transitions and evaluates risk.
    -   Manages approvals and creates or updates change tasks.
    -   Documents closure code and notes.
-   Evaluates change data quality based on defined policies or similar changes to maintain quality standards across change operations.

The ITSM MCP Server handles these employee experience capabilities for requesters:

-   Creates an incident, with knowledge base deflection that searches for self-service solutions before creating a ticket.
-   Checks the status and details of their own incidents and requested items.
-   Escalates an incident to raise its urgency.
-   Adds customer-visible comments on an incident or requested item.

The ITSM MCP Server handles these core on-call scheduling capabilities:

These on-call capabilities are inactive by default. To use them, you must first activate them.

-   Retrieves current on-call roster and identifies who is on call during a specified time period.
-   Checks personal on-call schedules and views upcoming shifts across rotation cycles.
-   Requests time off or shift coverage through the MCP client application.
-   Searches and retrieves on-call rotation details by team, location, or escalation group.
-   Manages on-call handoff and override requests with approval workflows.
-   Queries the ServiceNow Knowledge Graph to answer natural language questions about on-call schedules, coverage, and availability.

## ITSM MCP Server users

|Users|Description|
|-----|-----------|
|IT administrators|Activates the ITSM MCP Server.|
|Service desk agents, change managers, and fulfillers|Use the ITSM MCP Server to investigate incidents, manage change requests, perform updates, and move incidents and change requests through their lifecycle, without switching between windows or opening forms. Users ask questions through the MCP client application and request actions in the chat.|
|Employees and requesters|Use the ITSM MCP Server to create incidents, check the status of their own incidents and requested items, escalate incidents, and add comments, through an MCP client application, without opening the ServiceNow instance directly.|

## Server operation

The ITSM MCP Server operates as a secure intermediary between any MCP client application and the ServiceNow instance:

-   An ITSM MCP Server user asks a question using an MCP client.

    For example:

    -   An agent opens their MCP client application such as Moveworks or Claude and asks a question about an incident or a change request.
    -   An employee or requester opens their MCP client application such as Moveworks or Claude and asks a question about their own ticket.
-   The MCP client application sends the question to the ITSM MCP Server using the Model Context Protocol.
-   The ITSM MCP Server authenticates the user against the ServiceNow role-based access control.
-   The ITSM MCP Server retrieves the requested data or performs the requested action in the ServiceNow instance.
-   The ITSM MCP Server returns the result to the AI client application, which displays the result to the user.

