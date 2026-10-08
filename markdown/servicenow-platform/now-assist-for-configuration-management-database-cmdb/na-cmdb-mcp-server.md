---
title: Activate the CMDB MCP Server
description: Enable AI agents and other clients to securely access data and perform actions using the Model Context Protocol \(MCP\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-mcp-server.html
release: australia
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [MCP Server, Model Context Protocol, CMDB MCP]
breadcrumb: [Configure, ServiceNow Otto for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Activate the CMDB MCP Server

Enable AI agents and other clients to securely access data and perform actions using the Model Context Protocol \(MCP\).

## Before you begin

Before activating the CMDB MCP Server, confirm the following requirements are met.

-   You have MCP Platform Manager version 1.4 or later installed. Version 1.3 prevents MCP Server tools from being discoverable by AI clients.
-   The com.snc.cmdb.gen.ai plugin is active. CMDB Search, Create CI, Get Similar CI Classes, Explain CMDB Data Model, and Get CI Topology depend on it.

**Important:** If you also plan to use the Service Mapping tools bundled with this server, activate the com.sn.itom.sm.gen.ai plugin before installing the CMDB MCP Server application. The Service Mapping tool records are added only at install time; if the plugin is activated afterward, reinstall the CMDB MCP Server application to pick them up. For details, see .

Role required:

|MCP endpoint|Role required|
|------------|-------------|
|CMDB Search|sn\_cmdb\_user|
|Create CI|sn\_cmdb\_editor|
|Get Similar CI Classes|sn\_cmdb\_user|
|Get Impacted Items|itil, enforced by the Impact Analysis Skill capability rather than by this endpoint directly|
|Get CI Topology|None found; visibility follows the caller's own CMDB read access|
|Explain CMDB Data Model|sn\_cmdb\_user and sn\_data\_model\_nav.data\_model\_navigator\_read|

**Note:** Role checks for CMDB tools and Service Mapping tools are independent, even though both tool groups run under the same MCP server. A caller with only a CMDB role gets an authorization error on every Service Mapping tool, and a caller with only a Service Mapping role gets an authorization error on every CMDB tool.

## About this task

For an overview of the MCP Server and its supported clients and tools, see [CMDB MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-mcp-server-c.md).

## Procedure

1.  Navigate to **All** &gt; **Admin Center** &gt; **MCP Server Console**.

2.  On the Servers page of the Configuration console, select the **CMDB MCP Server** card and then select **Activate**.

3.  To control access to the server, set up OAuth credentials using the Inbound Integrations feature as described in [Inbound integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/inbound-integrations.md).

    For instructions on connecting an MCP client to the server, see [Connecting to an MCP server from an MCP client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/connect-mcp-server-client.md).


**Parent Topic:**[Configuring ServiceNow Otto for CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-configuring.md)

**Related topics**  


[CMDB MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-mcp-server-c.md)

[CMDB MCP Server tools reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-mcp-server-ref.md)

