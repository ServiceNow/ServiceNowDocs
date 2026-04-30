---
title: Legacy: Performance Analytics ITSM Dashboards
description: The ITSM Dashboards content pack provides several Platform Analytics Solutions that contain preconfigured dashboards. This content pack also includes several dashboards and indicators of its own. These dashboards contain actionable data visualizations that help you improve your business processes and practices.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Platform Analytics ITSM Dashboards, IT Service Management]
---

# Legacy: Performance Analytics ITSM Dashboards

The ITSM Dashboards content pack provides several Platform Analytics Solutions that contain preconfigured dashboards. This content pack also includes several dashboards and indicators of its own. These dashboards contain actionable data visualizations that help you improve your business processes and practices.

## ITSM Dashboard solutions

The ITSM Dashboards plugin \(com.snc.pa.itsm\_dashboards\) activates the following solutions, along with a set of additional dashboards:

-   [Change Management \(com.snc.pa.change\)](change-content-pack.md)
-   [Problem Management \(com.snc.pa.problem\)](problem-content-pack.md)
-   [Incident SLA \(com.snc.pa.sla\)](incident-sla-content-pack.md)
-   [Major Incident Management \(com.snc.pa.incident.mim\)](../../../product/incident-management/concept/major-incident-overview.md)
-   Fixed Costs \(com.snc.fixed\_costs\)

## Inactive dashboards

Some dashboards in this content pack are inactive when installed. Complete configuration and run [data collection jobs](https://www.servicenow.com/docs/access?context=now-platform-glossary&version=xanadu&pubname=xanadu-glossary&section=gloss-data-collector&ft:locale=en-US) before you activate these dashboards. You can activate dashboards in Dashboard Properties, accessible from the context menu. You have to assign an owner to the dashboard to activate it. For more information about configuring Platform Analytics Solutions, see [Configure Platform Analytics Solutions](https://www.servicenow.com/docs/access?context=configure-nowintel-solutions&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)

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


[Platform Analytics Solutions](https://www.servicenow.com/docs/access?context=content-packs-in-form-analytics&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)

[Activate your Performance Analytics subscription](https://www.servicenow.com/docs/access?context=c_PremiumPerformanceAnalytics&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)

