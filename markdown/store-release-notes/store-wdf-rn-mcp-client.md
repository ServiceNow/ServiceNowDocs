---
title: MCP Client release notes
description: Version history for the ServiceNow MCP Client application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-wdf-rn-mcp-client.html
release: store
topic_type: reference
last_updated: "2026-10-08"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Workflow Data Fabric version history release notes, ServiceNow Store version history release notes]
---

# MCP Client release notes

Version history for the ServiceNow® MCP Client application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.1.3 - October 2026**

    MCP Client APIs now support product-level identification and telemetry. Users can now specify a product when interacting with MCP Client APIs, enabling tracking and aggregation of usage across products. Telemetry events are emitted for both MCP operations and tool invocations, allowing measurement of adoption and usage. Each operation and tool call generates a corresponding telemetry event, capturing product, method, server, status, and tool name.

-   **Version 1.0.2 - July 2026**

    The MCP Client is the foundational connectivity layer for AI Agents on the Now Platform. It gives every ServiceNow application, on-Glide and off-Glide, a single governed path to invoke tools and access resources from any MCP-enabled server. Access is gated through AI Control Tower at runtime, meaning governance is not a configuration step teams can skip. It is wired into the execution path before any MCP call goes out. Developers can also invoke MCP Servers directly from server-side logic using the MCPClient Script Include, purpose-built for ServiceNow scripting contexts.


**Parent Topic:**[ServiceNow Store - Workflow Data Fabric version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-workflow-data-fabric-highlights.md)

