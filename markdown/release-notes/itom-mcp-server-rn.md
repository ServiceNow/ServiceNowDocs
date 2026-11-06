---
title: ITOM MCP Server Console release notes
description: The ServiceNow ITOM MCP Server Console lets agents fetch ITOM data and perform actions through an AI-enabled MCP Client using natural language, outside the ServiceNow UI.This release enables Event Management operators and administrators to investigate alerts, review CI reliability, assess service impact, and manage alert actions from their MCP Client. It also enables administrators to configure MID-less Health Log Analytics integrations without switching to the ServiceNow UI.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/itom-mcp-server-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [IT Operations Management, ITOM, MCP Server, MCP Server Console, release notes, ITOM, IT Operations Management, MCP Server, Console, store, release notes]
breadcrumb: [IT Operations Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# ITOM MCP Server Console release notes

The ServiceNow ITOM MCP Server Console lets agents fetch ITOM data and perform actions through an AI-enabled MCP Client using natural language, outside the ServiceNow UI.

## About ITOM MCP Server Console

-   Act on alerts through an AI-enabled MCP Client using natural language.
-   Assign, close, reopen, or acknowledge alerts in single or bulk actions.
-   Review the reliability status of a CI, including related incidents, alerts, and SLOs.
-   Request and execute alert remediation suggestions.
-   Set up MID-less log ingestion integrations for Health Log Analytics directly from your MCP Client.

See [Using the ITOM MCP Server Console to perform ITOM tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/use-itom-mcp-server.md) for more information.

The ITOM MCP Server Console includes AIOps, SRM, and LEAP tools. For details on LEAP tools, see [LEAP MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/aiops-leap-mcp-server-overview.md).

## Activation and other requirements

**Note:** ITOM MCP Server Console is available in the ServiceNow Store. For details, see the following activation information.

-   **Activation information**

    Install the ITOM MCP Server Console by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


**Parent Topic:**[IT Operations Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/it-operations-management-rn-landing.md)

## Version 1.1.0

This release enables Event Management operators and administrators to investigate alerts, review CI reliability, assess service impact, and manage alert actions from their MCP Client. It also enables administrators to configure MID-less Health Log Analytics integrations without switching to the ServiceNow UI.

### What's new

-   **[Resolve alerts without leaving your MCP Client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/itom-mcp-server-alert-actions.md)**

    Assign, close, reopen, acknowledge, and annotate alerts through natural-language prompts in your MCP Client application, eliminating context switching between tools. This reduces resolution time and keeps you focused on the incident at hand. The tool automatically detects whether your request applies to a single alert or an alert group, so you can coordinate action across multiple related alerts in one request.

-   **[Coordinate response to related alerts in your MCP Client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/itom-mcp-server-bulk-alert-actions.md)**

    Assign, close, reopen, or acknowledge multiple related alerts as a group in a single request from your MCP Client. When a widespread outage affects several systems, you can route all related alerts to the responsible team and add investigation notes simultaneously. This keeps your response coordinated without repetitive manual work.

-   **[Review service dependencies and incident impact in your MCP Client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/itom-mcp-server-ci-reliability.md)**

    Assess configuration item \(CI\) reliability status, topology, and incident impact directly from your MCP Client application through natural-language prompts. Assess which upstream and downstream services are affected by an alert, so your team understands the full scope of impact before escalating or deciding on remediation steps. Create service level objectives \(SLOs\) for CIs that don't have them yet, and monitor active SLOs and related alerts, all without navigating to the ServiceNow UI.

-   **[Get remediation suggestions in your MCP Client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/itom-mcp-server-alert-remediation.md)**

    Request a remediation suggestion for an alert through natural-language prompts in your MCP Client application. The tool uses your existing workflows and knowledge base articles to recommend the next step, so you can resolve issues faster without navigating back to the ServiceNow UI. Review the suggestion or follow the deep link back to Service Operations Workspace to confirm and execute the remediation action.

-   **[Set up MID-less log ingestion for HLA from your MCP Client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/itom-mcp-server-hla-ingest.md)**

    Create and configure MID-less log ingestion integrations for Health Log Analytics directly from your AI-enabled MCP Client application, without navigating to the Integrations Launchpad. Request integration creation, activation, renaming, and token rotation entirely through natural-language prompts. The MCP Client returns all endpoint and credential details needed to configure your collector, eliminating manual UI navigation for integration setup and credential management.


