---
title: Model Context Protocol connectors
description: Model Context Protocol \(MCP\) connectors in Connect Hub enable AI agents to access tools and data from external systems using a standardized communication protocol.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/model-context-protocol-connector.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: concept
last_updated: "2026-06-05"
reading_time_minutes: 3
breadcrumb: [Build integrations with connectors, Connect, Workflow Data Fabric Home, Workflow Data Fabric]
---

# Model Context Protocol connectors

Model Context Protocol \(MCP\) connectors in Connect Hub enable AI agents to access tools and data from external systems using a standardized communication protocol.

MCP is an open protocol that defines how AI agents communicate with external systems to discover and invoke tools, retrieve resources, and share context. By standardizing this communication layer, MCP allows AI agents to interact with a wide range of third-party applications without requiring custom integration logic for each one.

In Connect Hub, an MCP connector represents a configured connection between ServiceNow and an external system that exposes an MCP-compatible server. Once an MCP connector is set up, AI agents can use it to access the tools and capabilities that the external system provides, enabling coordinated, context-aware workflows across models and systems.

## MCP Registry

ServiceNow MCP Registry is a private registry where large language models \(LLMs\), AI agents, and teams discover and connect to approved MCP servers, finding the best tool for every business problem, governed at every step. The Registry enables AI models and humans query available MCP servers and select the ones best suited to solve a business problem. Every server exposed to an LLM is pre-approved in AICT, helping to ensure autonomous decisions never bypass enterprise governance. It works with AI Agent Studio, Claude, and so on. For more information, see [ServiceNow MCP Registry](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/mcp-registry.md).

## MCP connector registration methods for OAuth 2.1

Connect Hub supports two OAuth client registration methods for connecting to external systems: manual client registration and dynamic client registration. When the MCP registry does not include a connector for the system you need, you can define a custom connector. Connectors that are tested and approved by ServiceNow display a **Certified by ServiceNow** label in the registry.

Dynamic client registration automates the OAuth application setup between Connect Hub and the third-party provider. Instead of requiring you to create an OAuth application manually, the provider and Connect Hub negotiate the client credentials automatically as part of the connection flow. When a connector may probably require manual setup, the registry entry displays the label **Manual setup may be required** next to the connector name.

Dynamic client registration offers the following advantages over manual registration:

-   Credentials are managed by the provider and rotated automatically, reducing the risk of credential exposure.
-   The connection workflow is completed in fewer steps.

Manual client registration requires you to create and configure an OAuth application in the third-party system's developer settings before connecting the MCP connector. During this process, the third-party system issues Client ID and a Client secret, which you provide to Connect Hub to authorize the connection.

The MCP registry in Connect Hub includes connectors for a curated set of third-party systems. If the registry does not contain a connector for the system you need, you can define a custom connector by providing your own MCP endpoint URL and authentication configuration.

## Authentication methods for custom connectors

When creating a custom MCP connector, you select an authentication method that matches the security requirements of your external MCP server. The following authentication methods are supported:

-   **OAuth 2.1**: The recommended method for MCP connectors. Supports both Dynamic Client Registration, where the server auto-populates client details, and Manual Client Registration, where you supply the client credentials directly.
-   **API key**: Uses a static key issued by the third-party application to authenticate requests to the MCP server.
-   **Basic Authentication**: Authenticates using a username and password associated with the MCP server.

