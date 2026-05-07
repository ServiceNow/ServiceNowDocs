---
title: Use the ITSM MCP Server
description: Connect an AI-enabled MCP client application to your ServiceNow environment using the ITSM MCP Server to enable incident management for service desk agents and IT managers.
locale: en-US
release: australia
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: concept
last_updated: "2026-04-16"
reading_time_minutes: 1
keywords: [ITSM MCP Server, Model Context Protocol, AI integration, incident management, Now Assist, service desk agents, IT managers, natural language, AI clients, Claude, Microsoft Copilot]
audience: [administrator, user]
breadcrumb: [Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# Use the ITSM MCP Server

Connect an AI-enabled MCP client application to your ServiceNow environment using the ITSM MCP Server to enable incident management for service desk agents and IT managers.

## ITSM MCP Server overview

The ITSM MCP Server bridges your ServiceNow ITSM environment to any AI-enabled MCP client, also referred to as MCP client, such as Moveworks, or Claude. When agents use an MCP client to ask questions about incidents, the ITSM MCP server fetches data from the ServiceNow ITSM environment and performs actions on behalf of the agent—all through natural language conversation.

The server handles these core incident management capabilities:

-   Retrieves incident details based on the incident number.
-   Modifies incident details based on the incident number.
-   Looks up incident assignees and assignment groups.
-   Searches and retrieves similar records.

## ITSM MCP Server users

|Users|Description|
|-----|-----------|
|**IT administrators**|Activate the ITSM MCP Server.|
|**Service desk agents**|Use the ITSM MCP server to investigate incidents and perform updates without switching between windows or opening forms. Ask question through the MCP client application and request actions directly in the chat.|

## How the server works

The ITSM MCP Server operates as a secure intermediary between any MCP client application and the ServiceNow instance:

1.  An agent opens their MCP client application such as Moveworks or Claude and asks a question about an incident.
2.  The MCP client application sends the question to the ITSM MCP Server using the Model Context Protocol.
3.  The ITSM MCP Server authenticates the user against ServiceNow's role-based access control.
4.  The ITSM MCP Server retrieves the requested incident data or performs the requested action in the ServiceNow instance.
5.  The ITSM MCP Server returns the result to the AI client application, which displays it to the agent.

