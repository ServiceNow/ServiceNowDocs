---
title: Monitoring services and investigating issues
description: Operators use Service Observability to monitor the health of their services and to triage and manage incidents. They can view performance metrics from external application performance management \(APM\) systems in the context of an application service and its related CIs.
locale: en-US
release: xanadu
product: Service Observability
classification: service-observability
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Service Observability, ITOM Health, IT Operations Management]
---

# Monitoring services and investigating issues

Operators use Service Observability to monitor the health of their services and to triage and manage incidents. They can view performance metrics from external application performance management \(APM\) systems in the context of an application service and its related CIs.

## Overview of using Service Observability

Service Observability can display metrics from an APM instance in context of a service. Along with metrics for the service and information about related CIs, Service Observability can infer entities related to the service, like a host or database, and display their metrics. This functionality gives an operator a more holistic view of what might be affecting performance.

The **Overview** tab on the Service Details page shows high-level performance metrics for the service and other contextual information such as open alerts or incidents affecting the service. The **Observability** tab displays more detailed metrics from the APM for the service, along with metrics for inferred entities that are found through data mappings configured during setup. It also shows information about CIs related to those inferred entities. Instead of having to switch to an external tool, an operator can view those external metrics in the context of the Service Operations Workspace \(SOW\).

-   [View overall service health](../task/view-overall-service-health.md)

    In the **Overview** tab of the Service Details page in the SOW, view overall service health and related information, like alerts and changes.

-   [View service health metrics](../task/view-service-health-metrics.md)

    In the **Observability** tab, view more detailed service metrics, as well as metrics from related APM-monitored entities such as databases and hosts.


