---
title: Manage genAI skills using the CSM MCP Server
description: Use the CSM MCP Server to summarize cases, generate draft resolution notes, analyze sentiment, and create AI-drafted activity responses.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/customer-service-management/now-assist-for-csm/manage-genal-skills-csm-mcp-server.html
release: australia
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2026-08-24"
reading_time_minutes: 2
keywords: [MCP Server, genAI skills, case summarization, sentiment analysis, resolution notes]
breadcrumb: [Set up the CSM MCP Server, CSM MCP Server, ServiceNow Otto for CSM, Customer Service Management]
---

# Manage genAI skills using the CSM MCP Server

Use the CSM MCP Server to summarize cases, generate draft resolution notes, analyze sentiment, and create AI-drafted activity responses.

## Before you begin

Your system administrator must configure the integration between your MCP client application and your ServiceNow instance during setup.

The following table lists the roles required for each tool:

|Tool|Role required|Purpose|
|----|-------------|-------|
|case\_summarization|sn\_customerservice\_agent|Read CSM customer case records.|
|case\_summarization|sn\_customerservice.consumer\_agent|Read CSM consumer case records.|
|resolution\_notes\_generation|sn\_customerservice\_agent or sn\_customerservice.consumer\_agent|Read work notes and generate resolution notes for customer cases.|
|sentiment\_analysis|sn\_customerservice\_agent or sn\_customerservice.consumer\_agent|Read the case record and run sentiment analysis for permitted customer cases.|
|activity\_response|sn\_customerservice\_agent or sn\_customerservice.consumer\_agent|Read the case record and generate an AI-drafted activity response for permitted customer cases.|

Role required: sn\_customerservice\_agent or sn\_customerservice.consumer\_agent

## About this task

For detailed information on each tool, supported operations, and operation-specific parameters, see [CSM MCP Server tools reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/now-assist-for-csm/csm-mcp-server-tools-reference.md).

## Procedure

1.  Open your MCP client application, such as Moveworks or Claude on the web, that is connected to your ServiceNow instance using the CSM MCP Server.

    Your system administrator configures this integration during setup.

2.  To summarize a case or generate AI-drafted content, use the corresponding tools and operations.

    -   **case\_summarization:** Summarizes case activity, key actions, and current status.

        Example prompts:

        -   Give me the key actions on CS110086
        -   Get me the current status of CS110086
        -   Give me an overview of Case CS110086
        -   Get me up to speed on CS0001183
        -   What's going on with CS0001183?
        -   Show me the full details of CS0001183
        Tool Annotation: Read-only.

    -   **resolution\_notes\_generation:** Generates a draft resolution notes entry for the case.

        Example prompts:

        -   Give me a close up note on CS110086
        -   Can you generate the resolution notes for the case CS110086
        Tool Annotation: Read-only.

    -   **sentiment\_analysis:** Evaluates the sentiment of a CSM case using the Sentiment Analysis GenAI skill. Returns sentiment score, trend, and reasoning. Enforces record-level read access before invoking the skill.

        Example prompts:

        -   Show me the sentiment score on CS110086
        -   Get me the sentiment trend for CS110086
        Tool Annotation: Read-only.

    -   **activity\_response:** Generates an AI-drafted activity response for a CSM case using the Activity Response Generation skill. Supports three response modes: Respond, Follow-Up, Summarize.

        Example prompts:

        -   Give me the follow up on CS110086
        -   Get me the summary for CS110086
        Tool Annotation: Read-only.

3.  Review the MCP client application response.

    The MCP client application retrieves data from your ServiceNow instance and presents it in the chat. The response includes only data you have permission to access.


