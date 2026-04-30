---
title: AI Gateway
description: Explore the AI Gateway, its value and learn how to use and configure it for your MCP \(Model context protocol\) transactions.
locale: en-US
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Explore, AI Control Tower, Enable AI experiences]
---

# AI Gateway

Explore the AI Gateway, its value and learn how to use and configure it for your MCP \(Model context protocol\) transactions.

## Model Context Protocol

The Model Context Protocol \(MCP\) is a standardized client-server protocol that enables AI applications to discover and interact seamlessly with external tools, data sources, and systems. MCP facilitates communication between an AI host application \(AI Agent Studio\), an MCP Client embedded in the host, and one or more MCP servers that expose specific capabilities such as tools.

For more information on MCP, see [Model Context Protocol Client](https://www.servicenow.com/docs/bundle/zurich-intelligent-experiences/page/administer/model-context-protocol-client/reference/mcp-client.html)

## AI Gateway overview

AI Gateway enables governance, observability, and security for your MCP transactions. AI Gateway is designed to be platform agnostic, delivering the above-mentioned benefits both within ServiceNow \(AI Agent studio\) and in external agentic studios and hosts.

## Why Gateway

Enterprises are building unified AI across vendor boundaries. Their agentic workflows operate across platforms requiring governance.

AI Gateway offers:

-   Lifecycle management
-   Asset registry
-   Identity and access management
-   Secure authentication method \(OAuth 2.1\)
-   Observability

## Value of AI Gateway

With the increasing need of interoperability across different AI solutions across enterprises. AI Gateway provides a way for interoperability governance, observability &amp; security.

## Features and benefits

-   Enable tight governance and control of cross-platform resources such as MCP servers.
-   Enable enterprises to securely connect their agents to remote MCP servers, which work for any agent and MCP server.
-   Provide visibility into production metrics such as usage and latency.​

## Installation and prerequisites

Applications

-   Now Assist subscription \(required\)
-   AI Control Tower for Now Assist – Pro Plus license \(auto-installs sn\_awh\_config\)
-   AI Agent Studio \(required for MCP server intake in AI Gateway for AI Control Tower \(1.0.5\)\)

Plugins

-   sn\_ai\_governance \(version 5.0.6 or higher\)
-   sn\_telemetry\_data \(version 1.1.10 or higher\)

Roles

-   AI steward \[sn\_ai\_governance.ai\_steward\] - for approval workflows and policy management
-   AI Agent admin \[sn\_aia.admin\] – for configuring MCP servers as tools in AI Agent Studio

The AI Gateway application is automatically installed for customers who use AI Control Tower for Now Assist.

If you're using any generative AI features, you already have access to AI Gateway. The AI Gateway is included with all types of pro plus licenses. To use the features in AI Gateway, ensure that both AI Agent Studio and AI Control Tower are available in your instance.

## What to explore next

-   For information on the process flow of MCP servers, see [Process flow of MCP servers Via AI Gateway](process-flow-of-mcp-servers-via-ai-gateway.md)
-   For information on AI Gateway setup tab, see [MCP server record](view-the-mcp-server-record.md)
-   For information on AI Gateway in the configuration page, see [AI Gateway](ai-gateway.md)
-   For information on the roles in AI Control Tower and their role with AI Gateway, see [AI Control Tower roles](../reference/roles-installed-with-ai-control-tower.md)

