---
title: Legacy: Performance Analytics ITSM Dashboards
description: The ITSM Dashboards content pack provides several Platform Analytics Solutions that contain preconfigured dashboards. This content pack also includes several dashboards and indicators of its own. These dashboards contain actionable data visualizations that help you improve your business processes and practices.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Platform Analytics ITSM Dashboards, IT Service Management]
---

# Legacy: Performance Analytics ITSM Dashboards

The ITSM Dashboards content pack provides several Platform Analytics Solutions that contain preconfigured dashboards. This content pack also includes several dashboards and indicators of its own. These dashboards contain actionable data visualizations that help you improve your business processes and practices.

**Important:** Alternatively, executives and managers can use the metrics in the ITSM Success Dashboard to make informed decisions. For more information, see [Exploring ITSM Success Dashboard indicators](../../../product/itsm-success-dashboard/concept/explore-success-dashboard-indicators.md). Agents can use the IT Agent dashboard in Service Operations Workspace to obtain information about their work and their group's work. For more information, see [IT Agent dashboard for Service Operations Workspace](../../../product/service-operations-workspace/concept/it-agent-dashboard-sow.md).

Platform Analytics data visualizations use Performance Analytics [indicator](https://www.servicenow.com/docs/access?context=now-platform-glossary&version=yokohama&pubname=yokohama-glossary&section=gloss-indicator&ft:locale=en-US) data to show you data over time, helping you analyze your business processes and identify areas of improvement. With Platform Analytics Solutions, you can get value from Performance Analytics for your application with minimal setup. You can always create your own objects as well.

To enable the solution plugin for ITSM dashboards, an admin can navigate to **System Definitions** &gt; **Plugins** and activate the Performance Analytics - Content Pack - ITSM Dashboards plugin.

## ITSM Dashboard solutions

The ITSM Dashboards plugin \(com.snc.pa.itsm\_dashboards\) activates the following solutions, along with a set of additional dashboards:

-   [Change Management \(com.snc.pa.change\)](change-content-pack.md)
-   [Problem Management \(com.snc.pa.problem\)](problem-content-pack.md)
-   [Incident SLA \(com.snc.pa.sla\)](incident-sla-content-pack.md)
-   [Major Incident Management \(com.snc.pa.incident.mim\)](../../../product/incident-management/concept/major-incident-overview.md)
-   Fixed Costs \(com.snc.fixed\_costs\)

## Inactive dashboards

Some dashboards in this content pack are inactive when installed. Complete configuration and run [data collection jobs](https://www.servicenow.com/docs/access?context=now-platform-glossary&version=yokohama&pubname=yokohama-glossary&section=gloss-data-collector&ft:locale=en-US) before you activate these dashboards. You can activate dashboards in Dashboard Properties, accessible from the context menu. You have to assign an owner to the dashboard to activate it. For more information about configuring Platform Analytics Solutions, see [Configure Platform Analytics Solutions](https://www.servicenow.com/docs/access?context=configure-nowintel-solutions&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)

## Add Self-Service Analytic widgets to the ITSM dashboards

If you have Self-Service Analytics activated on an instance, you can add Self-Service analytics widgets to your Performance Analytics dashboards or a Service Portal. To obtain a ready-made set of indicators and breakdowns, activate the Self-Service Analytics PA \(**com.snc.pa.self\_service\_analytics**\) plugin. Find the Self-Service indicators through the Performance Analytics Admin Console, then create widgets and add them to your dashboard or portal. Also activate the \[SSA\] Self-Service Analytics data collection job.

-   **[Legacy: IT Executive dashboard](it-executive-dashboard.md)**  
See a high-level view across all of ITSM.
-   **[Legacy: IT Manager dashboard](itsm-it-manager-dashboard.md#)**  
Follow the daily and weekly progress of incidents, problems, and requests for your assignment groups.
-   **[Legacy: IT Agent dashboard](it-agent-dashboard.md)**  
View the open incidents, problems, and requests that belong to you and your assignment groups through personalized reports. You can also see which incidents that belong to your assignment groups exceed the Spotlight threshold.

**Parent Topic:**[Platform Analytics ITSM Dashboards](itsm-dashboards-content-pack-sd.md)

**Related topics**  


[Platform Analytics Solutions](https://www.servicenow.com/docs/access?context=content-packs-in-form-analytics&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)

[Activate your Performance Analytics subscription](https://www.servicenow.com/docs/access?context=c_PremiumPerformanceAnalytics&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)

