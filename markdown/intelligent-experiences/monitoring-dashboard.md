---
title: Monitoring dashboard
description: Explore MCP Server monitoring dashboard to review the performance and usage of the MCP servers and tools in a specific time frame.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/monitoring-dashboard.html
release: australia
topic_type: task
last_updated: "2026-08-20"
reading_time_minutes: 1
keywords: [Monitoring MCP server dashboard]
breadcrumb: [Configure, MCP Server Console, Enable AI experiences]
---

# Monitoring dashboard

Explore MCP Server monitoring dashboard to review the performance and usage of the MCP servers and tools in a specific time frame.

## Before you begin

Role required: sn\_mcp\_server.viewer

## About this task

Review the successes, failures, throttling incidents, and denial events associated with servers and tools for the specified time period. This enables a detailed understanding of performance metrics and issues encountered.

**Important:** The minimum version required is Australia patch 6 or Brazil patch 0.

## Procedure

1.  Navigate to **Admin** &gt; **MCP Server Console** &gt; **Configuration** &gt; **Monitoring**.

2.  Track the tools call volume and outcomes across your MCP servers.

    \[Omitted image "mcp-server-monitoring.png"\] Alt text: MCP server monitoring dashboard

3.  Choose to view the tools or server data.

4.  View the findings sorted by each tool used or by each server involved.

    -   Calls: Number of times the tool/server call was attempted
    -   Success: Number of times the tool/server was successively called
    -   Failed: Number of times the tool/server call failed. This count includes throttled, denied, and other failed calls
    -   Success rate: Percentage of successful tool/server calls
    -   Throttled: Number of calls that failed as they were over the call limit set by the platform or the server
    -   Denied: Calls denied due to authorization or policy
5.  You can also turn on the **Show per-server details** to sort and view server-wise tools data.


**Parent Topic:**[Configuring MCP Server Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-mcp-server-console.md)

