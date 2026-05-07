---
title: Manage incidents using the ITSM MCP Server with MCP client applications
description: Use the ITSM MCP Server to ask questions about incidents and perform updates through an MCP client application such as Moveworks or Claude.
locale: en-US
release: australia
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: task
last_updated: "2026-04-16"
reading_time_minutes: 1
keywords: [ITSM MCP Server, incident management, natural language prompts, AI workflow]
breadcrumb: [Use the ITSM MCP Server, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# Manage incidents using the ITSM MCP Server with MCP client applications

Use the ITSM MCP Server to ask questions about incidents and perform updates through an MCP client application such as Moveworks or Claude.

## About this task

The ITSM MCP Server allows you to modify and query incidents through MCP client applications connected to your ServiceNow instance. You can ask the AI client applications questions about incidents. The MCP tools retrieve data from your ServiceNow instance and perform actions on your behalf.

The following are examples of tools used to query incidents.

|Tools|Description|
|-----|-----------|
|**modify\_incident**|Modifies an existing incident record identified by incident number.|
|**get\_incident\_details**|Retrieves core fields of a single incident record number identified by the incident number.|
|**lookup\_users**|Searches and matches eligible assignees by name.|
|**search\_similar\_records**|Performs a semantic search to find incidents similar to the given query.|
|**lookup\_assignment\_groups**|Looks up assignment groups by name.|

## Before you begin

**Role required:** itil

## Procedure

1.  Open your MCP client application such as Moveworks, that is connected to your ServiceNow instance using the ITSM MCP Server.

    Your system administrator configures this integration during setup.

2.  Ask the AI tool a question about an incident.

    Use natural language to ask questions. Here are common types of prompts:

    -   **Get incident details:** "Get the status of incident INC0123456."
    -   **Find similar incidents:** "Show me incidents similar to INC0123456."
    -   **Modifies an existing incident:** "Add this work note to INC0123456: This incident was resolved successfully."
    -   **Look up users or assignment groups;**"Assign INC0123456 to Abel Tuter" or "Assign INC0123456 to the Network group."
3.  Review the MCP client application response.

    The MCP client application retrieves data from your ServiceNow instance and presents it in the chat. The response includes only data you have permission to access.


## What to do next

After you use the ITSM MCP Server to manage an incident, you can verify the changes in your ServiceNow instance connected to the AI client application to confirm the changes.

