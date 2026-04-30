---
title: Exploring Service Observability
description: Service Observability helps operations teams triage and manage incidents in a complex and distributed production system. It combines external application performance monitoring \(APM\) systems' telemetry with related data from the Configuration Management Database \(CMDB\) and displays both in a single workflow in the Service Operations Workspace \(SOW\).
locale: en-US
release: yokohama
product: Service Observability
classification: service-observability
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Service Observability, ITOM AIOps, IT Operations Management]
---

# Exploring Service Observability

Service Observability helps operations teams triage and manage incidents in a complex and distributed production system. It combines external application performance monitoring \(APM\) systems' telemetry with related data from the Configuration Management Database \(CMDB\) and displays both in a single workflow in the Service Operations Workspace \(SOW\).

## Service Observability overview

Service Observability displays health metrics in the SOW related to a given service. Metrics can be ingested from an external APM system and displayed alongside information for related configuration items in the CMDB.

Service Observability supports the following APM vendors:

-   Amazon CloudWatch
-   AppDynamics
-   Datadog
-   Dynatrace
-   Microsoft Azure Monitor
-   New Relic
-   Prometheus \(on-premise\)
-   SolarWinds on-premise
-   Splunk Observability

Service Observability supports the following databases:

-   MySQL
-   PostgreSQL \(not supported with Splunk\)
-   RDS \(Relational Database Service\) \(Amazon CloudWatch\)

After connecting an APM instance to Service Observability, map services in the CMDB to APM metrics using existing tags.

With this data mapping, Service Observability displays APM metrics for entities such as host or database along with details about related CI information. Operators use these metrics and contextual information, including current incidents and alerts, to assess service health.

For example, say you use Dynatrace to monitor your `checkout` service, and metrics from your database and host use the tag `checkout-service` to denote requests coming from that service. By mapping the `checkout` service CI to the APM data tagged with `checkout-service`, Service Observability retrieves metrics for those databases and hosts and CIs related to the service, then displays them together. Operators can pinpoint issues on entities related to the service and narrow down the mitigation process without having to leave the SOW.

## Service Observability users

<table id="table_y3t_vym_rdc"><thead><tr><th>

User

</th><th>

Description

</th></tr></thead><tbody><tr><td>

System admin

</td><td>

Version 1.5 only.

 System admins configure users and teams, register services to be monitored, connect Service Observability to APMs, and then map those services to that data. They can also view the data in the SOW

</td></tr><tr><td>

Service Observability admin

</td><td>

Version 1.6.x and later.Service Observability admins can configure users and teams, connect Service Observability to APMs, and then map services to that data. They can also view the data in the SOW. Admins can also customize dashboard templates used to display metrics and related information.

</td></tr><tr><td>

Operator/operations manager**Note:** These users must belong to an `srm` group type to see all data.

</td><td>

Operators use Service Observability when triaging incidents in the SOW. They can view basic health metrics for a service, along with related incidents, alerts, and changes. They can get more detailed information by navigating to the **Observability** tab to view additional service metrics, along with metrics from related entities, such as a host or database.

</td></tr></tbody>
</table>## Service Observability workflow

Admins configure Service Observability by registering services, connecting APM metrics, and then mapping the services to that data. Operators use Service Observability to determine if another related entity is causing issues surfaced by the service's performance.

As an admin, you:

1.  Determine the services to be monitored by Service Observability based on business criticality.
2.  Connect existing APM instances to Service Observability.
3.  Map services with APM metric data based on APM-based tags used on that data.
4.  Customize the templates used to display metric charts.

As an operator or manager, you:

1.  Spot an issue with a service while working in the SOW, for example, from an alert, the Service dashboard, or Express List, then navigate to the Service Details page.
2.  View overall health metrics for the service, along with related incidents, alerts, and changes. If one of the metrics seems unhealthy, navigate to the Observability tab.
3.  View more detailed service metrics, as well as information from related entities, to start root cause investigation. When finding that the issue is further down the system's stack, identify the ownership for that entity to start remediation.

## Service Observability benefits

<table id="table_bjt_vym_rdc"><thead><tr><th>

Benefit

</th><th>

Feature

</th><th>

Users

</th></tr></thead><tbody><tr><td>

Centralize critical signals and bridge workflows to increase agility and reliability: -   Connect data from external APMs
-   Map that data to CMDB services
-   View combined data in the SOW

</td><td>

-   [Connect a Service Observability data source](../task/connect-an-observability-data-source.md)
-   [Create and manage data mappings](../task/create-and-manage-observability-data-mappings.md)

.

</td><td>

Admins

</td></tr><tr><td>

Increase efficiency and reduce mean time to resolution \(MTTR\). View combined metrics from entities associated with a service to begin to determine blast radius and ownership of an incident.

</td><td>

[View service health metrics](../task/view-service-health-metrics.md)

</td><td>

Operators

</td></tr><tr><td>

See related changes to the system and alerts associated with a service in one place.

</td><td>

[View overall service health](../task/view-overall-service-health.md).

</td><td>

Operators

</td></tr><tr><td>

Customize dashboard templates.

</td><td>

[Customize Service Observability dashboard templates](../task/customize-service-observability-dashboard-templates.md)

</td><td>

Admins

</td></tr></tbody>
</table>## What to explore next

To learn more about configuring and using Service Observability, see:

-   [Configuring Service Observability](configuring-service-observability.md)
-   [View overall service health](../task/view-overall-service-health.md)
-   [View service health metrics](../task/view-service-health-metrics.md)
-   [Service Observability reference](../reference/service-observability-reference.md)

