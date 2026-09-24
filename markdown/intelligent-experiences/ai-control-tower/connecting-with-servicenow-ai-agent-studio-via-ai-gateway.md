---
title: Connecting with AI Agent Studio Via AI Gateway
description: Connecting with ServiceNow AI Agent Studio via AI Gateway.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-control-tower/connecting-with-servicenow-ai-agent-studio-via-ai-gateway.html
release: brazil
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Connect to MCP servers Via AI Gateway, AI Gateway, Exploring AI Control Tower \(legacy\), AI Control Tower \(legacy\), Establishing AI governance, Enable AI Experiences]
---

# Connecting with AI Agent Studio Via AI Gateway

Connecting with ServiceNow AI Agent Studio via AI Gateway.

## Before you begin

Role required: an\_aia.admin

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio**.

2.  Open an existing agent or create a new agent.

3.  Select **Edit**.

4.  Select **Tools**.

5.  Select **+Add a tool**.

6.  Select **+ New tool**.

7.  Select **Model Context Protocol**.

8.  Select the MCP server from the list.

    **Note:** In AWH for AI Control Tower \(2.0.0\), unapproved MCP Servers appear in the list but tools can't be fetched until the server is approved in AI Control Tower.

9.  Select the specific tools from the MCP server that the agent should use.

10. Select **Save**.


## Result

The agent is configured to use the MCP Server through AI Gateway. All requests from the agent to the MCP Server are routed through AI Gateway for governance, security, and observability.

