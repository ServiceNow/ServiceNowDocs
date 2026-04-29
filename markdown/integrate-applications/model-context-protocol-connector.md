---
title: Model Context Protocol connectors
description: Model Context Protocol \(MCP\) connectors in Connect Hub enable AI agents to access tools and data from external systems using a standardized communication protocol.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Build integrations with connectors, Connect, Workflow Data Fabric Home, Workflow Data Fabric]
---

# Model Context Protocol connectors

Model Context Protocol \(MCP\) connectors in Connect Hub enable AI agents to access tools and data from external systems using a standardized communication protocol.

MCP is an open protocol that defines how AI agents communicate with external systems to discover and invoke tools, retrieve resources, and share context. By standardizing this communication layer, MCP allows AI agents to interact with a wide range of third-party applications without requiring custom integration logic for each one.

In Connect Hub, an MCP connector represents a configured connection between ServiceNow and an external system that exposes an MCP-compatible server. Once an MCP connector is set up, AI agents can use it to access the tools and capabilities that the external system provides, enabling coordinated, context-aware workflows across models and systems.

## Authentication methods

When creating an MCP connector, you select an authentication method that matches the security requirements of your external MCP server. The following authentication methods are supported:

-   **OAuth 2.1**: The recommended method for MCP connectors. Supports both Dynamic Client Registration, where the server auto-populates client details, and Manual Client Registration, where you supply the client credentials directly.
-   **API key**: Uses a static key issued by the third-party application to authenticate requests to the MCP server.
-   **Basic Authentication**: Authenticates using a username and password associated with the MCP server.

