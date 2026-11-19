---
title: Integrating MCP server with third-party identity providers
description: Configure the ServiceNow Model Context Protocol \(MCP\) server to authenticate users through a third-party identity provider \(IDP\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/integrating-mcp-server-with-third-party-identity-providers.html
release: zurich
topic_type: concept
last_updated: "2026-06-19"
reading_time_minutes: 1
keywords: [MCP and third-party IDP]
breadcrumb: [Connect, MCP Server Console, Enable AI experiences]
---

# Integrating MCP server with third-party identity providers

Configure the ServiceNow® Model Context Protocol \(MCP\) server to authenticate users through a third-party identity provider \(IDP\).

When you integrate a third-party IDP with an MCP server, users authenticate through the external IDP instead of ServiceNow's native authentication. This process involves three phases:

1.  ServiceNow \(Glide\) configuration
2.  Third-part IDP setup
3.  Integration and testing

The first phase is ServiceNow \(Glide\) configuration that involves setting up the necessary tables and mappings within your ServiceNow instance. This has three steps:

1.  Configure the OIDC provider
2.  Create the MCP server
3.  Map the resource to the IDP

The second phase is Third-party IDP setup that involves setting up the application and authorization server within the IDP. This has three steps:

1.  Account setup
2.  Create an app integration
3.  Configure the authorization server

The final phase is Integration and testing that involves connecting the MCP client \(such as Claude Desktop\) to the configured systems. This involves three steps:

1.  Connect to the MCP client
2.  Authenticate
3.  Verify tool calls

-   **[ServiceNow\(Glide\) configuration for IDP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/servicenow-configuration-for-idp.md)**  
This process involves setting up the necessary tables and mappings within your ServiceNow instance. This includes configuring ServiceNow, creating the MCP server, and connecting the MCP client.
-   **[Integrate and test IDP with MCP server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/integrate-and-test-idp-with-mcp-server.md)**  
This phase within integration of MCP server with IDP involves connecting the MCP client \(such as Claude Desktop\) to the configured systems.

**Parent Topic:**[Connecting to an MCP server from an MCP client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/connect-mcp-server-client.md)

**Related topics**  


[Integrate and test IDP with MCP server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/integrate-and-test-idp-with-mcp-server.md)

[ServiceNow\(Glide\) configuration for IDP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/servicenow-configuration-for-idp.md)

