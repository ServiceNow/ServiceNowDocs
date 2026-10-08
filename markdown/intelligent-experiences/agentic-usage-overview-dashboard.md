---
title: Agentic Usage Overview Dashboard
description: Monitor usage from inbound agentic connections to MCP servers from the Agentic Usage Overview Dashboard.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/agentic-usage-overview-dashboard.html
release: brazil
topic_type: concept
last_updated: "2026-09-28"
reading_time_minutes: 2
keywords: [Agentic Usage Overview Dashboard, Action Fabric, MCP client, record access, flow execution]
breadcrumb: [Extending AI with external systems and providers, Enable AI Experiences]
---

# Agentic Usage Overview Dashboard

Monitor usage from inbound agentic connections to MCP servers from the Agentic Usage Overview Dashboard.

The Agentic Usage Overview Dashboard contains visualizations that help you assess the usage from Model Context Protocol \(MCP\) clients calling MCP servers in MCP Server Console.

The Agentic Usage Overview Dashboard \(sn\_agentic\_usage\) is active by default. You can access the dashboard by navigating to **All** &gt; **Agentic Usage** &gt; **Agentic Usage Overview Dashboard**. With the sn\_agentic\_usage.user or sn\_agentic\_usage.admin role, you can view usage data across two tabs: Record Access and Flow Execution.

\[Omitted image "agentic-usage-dashboard.png"\] Alt text: Agentic Usage Overview Dashboard showing the Record Access tab with daily and monthly bar charts and filter controls for MCP client and table.

## Record Access tab

The Record Access tab shows the number of records accessed through MCP servers. Use this tab to monitor record access volume over time and filter by MCP client or table. Select a bar or a point on a line chart to drill down to the records accessed with any currently applied filters retained.

|Visualization|Description|
|-------------|-----------|
|Record Access \(Daily\)|The number of records accessed for each day over the last 30 days.|
|Record Access \(Monthly\)|The number of records accessed for each month over the last 13 months.|
|Record Access by MCP Client \(Last 30 days\)|A trend line of records accessed by MCP client over the last 30 days.|
|Record Access by Table \(Last 30 days\)|A trend line of records accessed by table over the last 30 days.|

## Flow Execution tab

The Flow Execution tab shows the number of flows executed through MCP servers. Use this tab to monitor flow execution volume over time and filter by MCP client or flow name. Select a bar or a point on a line chart to drill down to the flows executed with any currently applied filters retained.

|Visualization|Description|
|-------------|-----------|
|Flow Execution \(Daily\)|The number of flows executed for each day over the last 30 days.|
|Flow Execution \(Monthly\)|The number of flows executed for each month over the last 13 months.|
|Flow Execution by MCP Client \(Last 30 days\)|A trend line of flows executed by MCP client over the last 30 days.|

**Related topics**  


[MCP Server Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown)

