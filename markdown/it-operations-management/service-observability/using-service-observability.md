---
title: Monitoring services and investigating issues
description: Operators use Service Observability to monitor the health of their services and to triage and manage incidents. They can view performance metrics from external observability monitoring systems in the context of an application service and its related CIs \(Configuration Item\).
locale: en-US
release: australia
product: Service Observability
classification: service-observability
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service Observability, ITOM AIOps, IT Operations Management]
---

# Monitoring services and investigating issues

Operators use Service Observability to monitor the health of their services and to triage and manage incidents. They can view performance metrics from external observability monitoring systems in the context of an application service and its related CIs \(Configuration Item\).

## Overview of using Service Observability

Service Observability can display metrics from an observability monitoring instance in context of a service. Along with metrics for the service and information about related CIs, Service Observability can infer entities related to the service, like a host or database, and display their metrics. This functionality gives an operator a more holistic view of what might be affecting performance.

The **Overview** tab on the Service Details page shows high-level performance metrics for the service and other contextual information such as open alerts or incidents affecting the service. The **Observability** tab displays more detailed metrics from the observability system for the service, along with metrics for inferred entities that are found through data mappings configured during setup. It also shows information about CIs related to those inferred entities. Instead of having to switch to an external tool, an operator can view those external metrics in the context of the Service Operations Workspace \(SOW\).

**Note:** Operators can also use the [Analyze a dashboard in Service Observability](../../now-assist-itom/concept/analyze-a-dashboard-in-service-observability.md) and the [Analyze service health in Service Observability](../../now-assist-itom/concept/analyze-service-health-in-service-observability.md) Now Assist AI skills to generate an analysis for them.

-   [View overall service health](../task/view-overall-service-health.md)

    In the **Overview** tab of the Service Details page in the SOW, view overall service health and related information, like alerts and changes.

-   [View service health metrics](../task/view-service-health-metrics.md)

    In the **Observability** tab, view more detailed service metrics, as well as metrics from related entities such as databases, hosts, and network components.


