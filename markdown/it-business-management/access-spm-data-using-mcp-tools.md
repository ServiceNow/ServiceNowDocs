---
title: Access Strategic Portfolio Management data using MCP tools
description: Use MCP tools to query live Strategic Portfolio Management data — including at-risk goals, portfolio plan insights, project insights, and project risks — from any MCP-compatible AI assistant.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/access-spm-data-using-mcp-tools.html
release: australia
topic_type: task
last_updated: "2026-06-12"
reading_time_minutes: 1
keywords: [MCP tools, Strategic Portfolio Management, portfolio insights, project insights]
breadcrumb: [Use, MCP for Strategic Portfolio Management, Strategic Portfolio Management]
---

# Access Strategic Portfolio Management data using MCP tools

Use MCP tools to query live Strategic Portfolio Management data — including at-risk goals, portfolio plan insights, project insights, and project risks — from any MCP-compatible AI assistant.

## Before you begin

Role required: sn\_align\_core.ap\_read\_only, or sn\_gf.goal\_user\_read, or it\_project\_manager

## About this task

When you request information, the relevant tool among the available MCP tools gathers insights about your projects and portfolios. For a list of available tools, see [Exploring MCP for Strategic Portfolio Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/exploring-spm-mcp-server.md).

**Note:** This procedure uses Claude as an example AI assistant. Steps may vary depending on the AI client you use.

## Procedure

1.  Open the Claude application on your computer.

2.  Start a chat by sending a message such as `Show me goals owned by Alex`.

    The **Get Goals** tool retrieves the goals owned by the specified user. Results include only goals from portfolio plans that you own.

    \[Omitted image "promt-show-goals-owned-by-megan.png"\] Alt text: Claude chat showing goals retrieved by the Get Goals MCP tool.

3.  Continue the conversation to retrieve additional data — for example, send `Show me insights for the first goal`.

    The **Generate Goal Insights** tool retrieves insights for the specified goal.

    \[Omitted image "prompt-show-me-insights-for-first-goal2.png"\] Alt text: Claude chat showing the first part of goal insights returned by the Generate Goal Insights MCP tool.

    \[Omitted image "promt-show-goals-owned-by-megan.png"\] Alt text: Claude chat showing the second part of goal insights returned by the Generate Goal Insights MCP tool.

4.  Continue the conversation with additional prompts to retrieve the data you need.


