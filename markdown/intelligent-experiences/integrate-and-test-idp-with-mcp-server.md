---
title: Integrate and test IDP with MCP server
description: This phase within integration of MCP server with IDP involves connecting the MCP client \(such as Claude Desktop\) to the configured systems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/integrate-and-test-idp-with-mcp-server.html
release: australia
topic_type: task
last_updated: "2026-06-19"
reading_time_minutes: 1
breadcrumb: [Integrating MCP server with third-party identity providers, Connect, MCP Server Console, Enable AI experiences]
---

# Integrate and test IDP with MCP server

This phase within integration of MCP server with IDP involves connecting the MCP client \(such as Claude Desktop\) to the configured systems.

## Before you begin

Role required: admin

## Procedure

1.  Connect the MCP client
2.  Navigate to your MCP client and go to **Manage Connectors** &gt; **Add a custom connector**.

    For example, open Claude Desktop.

3.  Enter the **Remote MCP Server URL** from your ServiceNow MCP server console.

4.  Enter the **Client ID** and **Client Secret** from your third-party IDP application configuration.

5.  Authenticate
6.  Select **Connect** and authenticate with your third-party IDP credentials.

    You're redirected to the IDP login page. Enter your credentials and verify.

7.  Verify tool calls
8.  Test your tool calls to verify the connection is working correctly.


## Result

Your MCP server is now configured to authenticate users through the third-party IDP. Users who connect an MCP client to this server are redirected to the IDP to authenticate.

**Parent Topic:**[Integrating MCP server with third-party identity providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/integrating-mcp-server-with-third-party-identity-providers.md)

