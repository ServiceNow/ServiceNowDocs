---
title: Activate the CMDB MCP Server
description: Enable AI agents and other clients to securely access data and perform actions using the Model Context Protocol \(MCP\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-mcp-server.html
release: zurich
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [MCP Server, Model Context Protocol, CMDB MCP]
breadcrumb: [Configure, ServiceNow Otto for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Activate the CMDB MCP Server

Enable AI agents and other clients to securely access data and perform actions using the Model Context Protocol \(MCP\).

## Before you begin

Role required:

|MCP endpoint|Role required|
|------------|-------------|
|CMDB Search|sn\_cmdb\_user|
|Create CI|sn\_cmdb\_editor|
|Get Similar CI Classes|sn\_cmdb\_user|
|Get Impacted Items|itil, enforced by the Impact Analysis Skill capability rather than by this endpoint directly|
|Get CI Topology|None found; visibility follows the caller's own CMDB read access|
|Explain CMDB Data Model|sn\_cmdb\_user and sn\_data\_model\_nav.data\_model\_navigator\_read|

## About this task

For an overview of the MCP Server and its supported clients and tools, see [CMDB MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-mcp-server-c.md).

## Procedure

1.  Navigate to **All** &gt; **Admin Center** &gt; **MCP Server Console**.

2.  On the Servers page of the Configuration console, select the **CMDB MCP Server** card and then select **Activate**.

3.  To control access to the server, set up OAuth credentials using the Inbound Integrations feature as described in [Inbound integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/inbound-integrations.md).

    For instructions on connecting an MCP client to the server, see [Connecting to an MCP server from an MCP client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/connect-mcp-server-client.md).


**Parent Topic:**[Configuring ServiceNow Otto for CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-configuring.md)

**Related topics**  


[CMDB MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-mcp-server-c.md)

[CMDB MCP Server tools reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-mcp-server-ref.md)

