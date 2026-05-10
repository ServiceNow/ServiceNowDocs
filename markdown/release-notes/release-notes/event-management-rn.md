---
title: Event Management release notes
description: The ServiceNow Event Management application helps you to identify health issues across the datacenter on a single management console. Event Management was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
---

# Event Management release notes

The ServiceNow® Event Management application helps you to identify health issues across the datacenter on a single management console. Event Management was enhanced and updated in the Australia release.

## Event Management highlights for the Australia release

-   Streamline Event Management setup with the new AI-guided Implementation Planner, helping admins configure ITOM AIOps faster and more accurately.
-   Enable smarter alert grouping based on CMDB service relationships, with thresholds and seed prerequisites to reduce noise and improve operational efficiency.
-   Enhance alert grouping by unifying Health Log Analytics and Event Management alerts, helping you reduce noise and act on alerts with greater confidence.
-   Support OpenTelemetry \(OTel\) metrics through the MID Server API to simplify metric ingestion and enhance anomaly detection capabilities.

-   **[ServiceNow Store updates for Event Management and Service Operations Workspace](https://store.servicenow.com/store/apps?q=ITOM)**

    Some apps are updated monthly or quarterly via the ServiceNow Store. For information about cumulative release notes and compatibility information, see the ServiceNow Store version details:

    -   [Event Management](https://store.servicenow.com/store/app/e1a9af221b246a50a85b16db234bcbcb#releaseNotes)
    -   [Integrations Launchpad](https://store.servicenow.com/store/app/a21ae3e21b246a50a85b16db234bcb4d#releaseNotes)
    -   [Express List](https://store.servicenow.com/store/app/98e8672e1be06a50a85b16db234bcb52#releaseNotes)
    -   [Alert Automation](https://store.servicenow.com/store/app/98e8672e1be06a50a85b16db234bcb52#releaseNotes)
    -   [Service Operations Workspace \(SOW\) for ITOM](https://store.servicenow.com/store/app/98e8672e1be06a50a85b16db234bcb52#releaseNotes)

See [Event Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/c_EM.md) or [Service Operations Workspace for ITOM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-operations-workspace-for-itom-apps/sow-landing-page-itom.md) for more information.

**Important:** Event Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   **[Unified alert grouping across Event Management and HLA](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-operations-workspace-for-itom-apps/group-alert-sow-itom.md)**

    Improve alert quality, reduce noise, and achieve higher compression to act faster on issues by grouping Health Log Analytics and Event Management alerts.

-   **[Explicit node-based control for CI binding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-operations-workspace-for-itom-apps/enrich-alert-sow-itom.md)**

    Increase binding accuracy and reliability and improve alert-to-CI binding with explicit node-based control, configurable node-field usage, enhanced mapping logic, and backward-compatible updates.


## UI changes

-   **Coral theme**

    The Coral theme has been improved to enhance usability across web, mobile, and portal experiences that use Next Experience and Core UI:

    -   A fully overhauled color system for smoother gradients and better contrast.
    -   Softer outlines and more rounded components for a modern, accessible look.
    -   A significantly improved dark mode with deeper blue tones for reduced eye strain.
    -   New AI gradient styles and subtle animations to highlight intelligent features.
    -   Smarter focus behavior that reduces visual clutter for mouse users.

## Deprecations

-   Alert Clustering Definitions \(ACD\) have been deprecated and fully replaced by Alert Automation in Service Operations Workspace. All existing configurations remain supported with full feature parity.
-   Service Management Dashboard is now deprecated and no longer supported or available for new activation. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.

## Activation information

Event Management is available with activation of the Event Management plugin \(com.glideapp.itom.snac\). For details, see [Request Event Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/t_EMActivatePlugin.md).

## Related ServiceNow applications and features

-   **[Metric Explorer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/metric-intelligence/agent-workspace-ops-intelligence.md)**

    ServiceNow® Agent Workspace for [Metric Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/metric-intelligence/operational-metrics.md) provides a central interface that enables you to view the health of a CI associated with an alert. Health details for a CI include various metric charts with control bounds and aggregations for single score charts.


**Parent Topic:**[IT Operations Management release notes](it-operations-management-rn-landing.md)

