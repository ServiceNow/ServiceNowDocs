---
title: Service Mapping release notes
description: The ServiceNow Service Mapping application discovers all application services in your organization and builds a comprehensive map of all configuration items used in these application services. See the following sections for release notes by version.The September 2026 store release introduces MCP Server integration and a Lightweight Service Model to improve performance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/service-mapping-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [ITOM Visibility release notes, IT Operations Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Service Mapping release notes

The ServiceNow® Service Mapping application discovers all application services in your organization and builds a comprehensive map of all configuration items used in these application services. See the following sections for release notes by version.

## About Service Mapping

-   AI-powered features in Service Mapping help administrators automate service map creation, connect business applications to discovered services, and query live service topology using natural language.
-   Multi-source service mapping combines data from multiple discovery methods to create a single, comprehensive service map that provides complete visibility into your organization's hybrid IT infrastructure.
-   The Lightweight Service Model is an optimized architecture for storing and determining service topology. It maintains current service data without storing historical snapshots, reducing storage overhead and improving performance for large configuration item inventories.

See [Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/c_ServiceMappingOverview.md) for more information.

## Activation and other requirements

-   **Activation information**

    For information on activating Service Mapping, see [Request Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/t_ActivateServiceMappingPlugin.md).For information on activating and updating Service Mapping Plus and AI Agents for Service Mapping, visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/06a71b1367e4130051c9027e2685ef1e/1.6.0?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%26q%3DPatterns&sl=sh).

    AI capabilities in Service Mapping require additional procedures for activation. For detailed information, see:

    -   [Activate AI Agents for Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/activate-sm-ai-agents.md)
    -   [Activate the Service Mapping Candidate skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/activate-sm-candidate-skill.md)
    -   [Activate the Service Mapping Candidates Impact skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/activate-sm-candidates-impact-skill.md)
    -   [Activate the CMDB MCP Server for Service Mapping tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/activate-sm-mcp-server.md)

**Parent Topic:**[ITOM Visibility release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/itom-visibility-rn.md)

## Version 1.24.4

The September 2026 store release introduces MCP Server integration and a Lightweight Service Model to improve performance.

### What's new

-   **[Service Mapping MCP tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/service-mapping-mcp-server.md)**

    The Service Mapping tools, delivered as part of the CMDB MCP Server plugin, version 1.0.0, expose live application service data and enable AI clients such as Claude to query service topology, identify mapping gaps, and create new application services in natural language.

-   **[Service Mapping Lightweight Service Model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/sm-lightweight-service-model.md)**

    Starting Service Mapping Plus version 1.24.4, you can improve service mapping performance by converting your Dynamic and Tag-Based services to Lightweight.


