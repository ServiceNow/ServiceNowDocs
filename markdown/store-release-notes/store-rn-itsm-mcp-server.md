---
title: ITSM MCP Server release notes
description: Version history for the ServiceNow ITSM MCP Server application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itsm-mcp-server.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - IT Service Management version history release notes, ServiceNow Store version history release notes]
---

# ITSM MCP Server release notes

Version history for the ServiceNow® ITSM MCP Server application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.2.2 - September 2026**
    -   ITSM MCP Server is built on the ServiceNow platform framework that exposes incident, change, and request management capabilities to any MCP-compatible AI client. The server is packaged as an ITSM MCP plugin with a dependency on Now Assist, providing a standardized integration surface for external AI tools.
    -   Key Design Principles
        -   Tiered rollout: Start with Incident Management \(minimum commitment\), expand to Change and Request Management
        -   Platform-native: Built on ServiceNow's platform framework, leveraging existing APIs and security model
        -   Clear server purpose: Descriptive server identity and tool descriptions so MCP clients \(e.g., Claude, CoPilot\) can effectively discover and match capabilities
        -   Now Assist for ITSM dependency: Plugin requires Now Assist capabilities, aligning with the ServiceNow AI platform strategy
        -   Existing tool reuse: Incorporate existing incident-related tools from prior work \(Now Assist skills, Moveworks Service Operations Assistant for Fulfillers\) and extend with change/request tools
    -   MCP client should be able to query any information within the context of an incident.

**Parent Topic:**[ServiceNow Store - IT Service Management version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itsm.md)

