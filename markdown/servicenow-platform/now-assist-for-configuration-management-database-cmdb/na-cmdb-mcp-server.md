---
title: Activate the Now Assist CMDB MCP server
description: Enable Al agents and other clients to securely access data and perform actions using the Model Context Protocol \(MCP\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-mcp-server.html
release: australia
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2026-05-04"
reading_time_minutes: 1
breadcrumb: [Configure, Now Assist for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Activate the Now Assist CMDB MCP server

Enable Al agents and other clients to securely access data and perform actions using the Model Context Protocol \(MCP\).

## Before you begin

Role required:

-   CMDB Search MCP endpoint: role sn\_cmdb\_user
-   Create CI MCP endpoint: sn\_cmdb\_editor
-   Get\_SimilarCI\_Classes for creation MCP endpoint: sn\_cmdb\_user

## About this task

The MCP server supports the Claude Desktop and Moveworks MCP clients. The CMDB Search, Create CI, and Get\_SimilarCI\_Classes for creation agents are supported.

Supported tools:

-   CMDB Search: Searches the CMDB for Cls based on the user utterance.
-   Get\_SimilarCI\_Classes for creation: Finds Cl classes that match a specified name or keyword. Use this tool before creating a Cl to identify the correct technical class name and its required attributes. The description will be used by MCP clients to determine when to call this tool.
-   Create CI: Creates a new CI for a specified Cl class with the provided attributes. Before using this tool, use Get\_SimilarCI\_Classes for creation to confirm the correct class name and required fields.

## Procedure

1.  Navigate to **All** &gt; **Admin Center** &gt; **MCP Server Console**.

2.  On the Servers page of the Configuration console, select the **Now Assist CMDB MCP Server** card and then select **Activate**.

3.  To control access to the server, set up OAuth credentials using the Inbound Integrations feature as described in .

    See client documentation for configuration and use instructions.


**Parent Topic:**[Configuring Now Assist for CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-configuring.md)

