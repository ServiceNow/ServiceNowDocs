---
title: View MCP server logs
description: Troubleshoot MCP server connections and tool calls by enabling logging for MCP servers and reviewing the logs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/view-mcp-server-logs.html
release: australia
topic_type: task
last_updated: "2026-10-15"
reading_time_minutes: 1
keywords: [MCP server logs, System Log, syslog, glide.log.off\_glide\_ingestion.enabled]
breadcrumb: [Configure, MCP Server Console, Extending AI with external systems and providers, Enable AI Experiences]
---

# View MCP server logs

Troubleshoot MCP server connections and tool calls by enabling logging for MCP servers and reviewing the logs.

## Before you begin

To enable logging MCP server activities, set the **glide.log.off\_glide\_ingestion.enabled** system property to true. The logs don't include activity that occurs before you enable the system property. For more information, see [Available system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Logs** &gt; **System Log** &gt; **All**.

2.  Use the condition builder to filter the Log list to **\[Source\] is \[mcp-server\]** to view MCP server activity only.


**Parent Topic:**[Configuring MCP Server Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/configuring-mcp-server-console.md)

**Related topics**  


[System log](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/r_SystemLogs.md)

