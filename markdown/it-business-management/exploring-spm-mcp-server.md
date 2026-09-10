---
title: Exploring MCP for Strategic Portfolio Management
description: With MCP for Strategic Portfolio Management, strategy/PMO leaders, portfolio managers, and project managers can access goal insights, portfolio insights, project insights, status reports, and risk in projects directly in their AI client and planning workflows — without opening the ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/exploring-spm-mcp-server.html
release: australia
topic_type: concept
last_updated: "2026-06-03"
reading_time_minutes: 2
keywords: [explore]
breadcrumb: [MCP for Strategic Portfolio Management, Strategic Portfolio Management]
---

# Exploring MCP for Strategic Portfolio Management

With MCP for Strategic Portfolio Management, strategy/PMO leaders, portfolio managers, and project managers can access goal insights, portfolio insights, project insights, status reports, and risk in projects directly in their AI client and planning workflows — without opening the ServiceNow instance.

## MCP for Strategic Portfolio Management overview

The Strategic Portfolio Management \(SPM\) Model Context Protocol \(MCP\) server connects an AI assistant such as Claude to your ServiceNow instance. Ask natural language to retrieve project data without navigating through tabs and reports.

## MCP for Strategic Portfolio Management personas

|Personas|Description|
|--------|-----------|
|Strategy leader and PMO leader|Queries at-risk goals, tracks strategic objectives, and retrieves goal insights to monitor alignment between business strategy and execution — directly from an AI assistant.|
|Product manager|Accesses goal and portfolio data to prioritize, plan, and roadmap the work and track their progress.|
|Portfolio manager|Retrieves portfolio plans, reviews their insights highlighting delayed projects, dependencies, resource allocation and timelines.|
|Project manager|Queries project data, generates AI status reports, identifies risks, and surfaces recommendations to help keep projects on schedule and within budget.|

## Available tools

Access Strategic Portfolio Management data and ServiceNow Otto skills as MCP tools, enabling LLM agents to query and process goals, portfolio plans, and projects.

The following tools are available:

|Tool name \[ID\]|Description|
|----------------|-----------|
|Get Goals \(sn\_spm\_mcp.get\_goals\)|Retrieves goals and objectives, providing foundational data for analysis and planning.|
|Generate Goal Insights \(sn\_spm\_mcp.generate\_goal\_insights\)|Generates AI-powered insights for goals and targets by cross-referencing historical data and identifying trends.|
|Get Portfolio Plans \(sn\_spm\_mcp.get\_portfolio\_plans\)|Retrieves portfolio plans, including resource allocation and timeline details, to support strategic decision-making.|
|Generate Portfolio Insights \(sn\_spm\_mcp.generate\_portfolio\_insights\)|Generates portfolio insights, including at-risk projects, delayed starts and ends, and dependencies, to highlight potential bottlenecks.|
|Generate Project Insights \(sn\_spm\_mcp.generate\_project\_insights\)|Detects project risks, analyzes status trajectory using predictive modeling, and provides recommendations to mitigate delays.|
|Get Projects \(sn\_spm\_mcp.get\_projects\)|Retrieves projects with associated metadata such as ownership, deadlines, and budget constraints.|
|Get AI Status Report \(sn\_spm\_mcp.get\_ai\_status\_report\)|Generates a Red, Amber, Green \(RAG\) status report across resources, cost, schedule, and scope, using color-coded indicators to prioritize critical issues.|
|Identify Project Risks \(sn\_spm\_mcp.identify\_project\_risks\)|Detects AI-identified RIDAC risks and saves them to the risk table as AI drafts.|

## What to explore next

To learn more about configuring and using MCP for Strategic Portfolio Management, see the following topics.

-   [Configuring MCP for Strategic Portfolio Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/configuring-spm-mcp-server.md)
-   [Using MCP for Strategic Portfolio Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/using-spm-mcp-server.md)
-   [MCP for Strategic Portfolio Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/reference-spm-mcp-server.md)

