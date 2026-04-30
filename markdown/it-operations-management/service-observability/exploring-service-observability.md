---
title: Exploring Service Observability
description: Service Observability helps operations teams triage and manage incidents in a complex and distributed production system. It combines external observability monitoring systems' telemetry with related data from the Configuration Management Database \(CMDB\) and displays both in a single workflow in the Service Operations Workspace \(SOW\).
locale: en-US
release: zurich
product: Service Observability
classification: service-observability
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Service Observability, ITOM AIOps, IT Operations Management]
---

# Exploring Service Observability

Service Observability helps operations teams triage and manage incidents in a complex and distributed production system. It combines external observability monitoring systems' telemetry with related data from the Configuration Management Database \(CMDB\) and displays both in a single workflow in the Service Operations Workspace \(SOW\).

## Service Observability overview

Service Observability displays application, infrastructure, and network health metrics in the SOW related to a given service. Metrics can be ingested from an external observability vendor \(application, network, and cloud monitors\) and displayed alongside information for related configuration items in the CMDB.

Service Observability supports the following observability vendors:

-   Amazon CloudWatch
-   AppDynamics
-   Cisco ThousandEyes synthetic tests
-   Datadog
-   DynatraceSaaS and on-premise \(both Classic and Grail environments\)
-   Microsoft Azure Monitor
-   New Relic
-   Prometheus on-premise
-   SolarWinds on-premise
-   Splunk Observability and logs from Splunk Enterprise
-   Zabbix on-premise

Service Observability supports the following databases:

-   MySQL
-   PostgreSQL \(not supported with Splunk\)
-   RDS \(Relational Database Service\) for Amazon CloudWatch

After connecting an observability vendor to Service Observability, you map services in the CMDB to observability metrics using existing tags.

With this data mapping, Service Observability displays metrics for entities such as host, database, or network components, along with details about related CI information. Operators use these metrics and contextual information, including current incidents and alerts, to assess service health.

**Note:** Operators can also use the [Analyze a dashboard in Service Observability](../../now-assist-itom/concept/analyze-a-dashboard-in-service-observability.md) and the [Analyze service health in Service Observability](../../now-assist-itom/concept/analyze-service-health-in-service-observability.md) Now Assist AI skills to generate an analysis for them.

For example, say you use Dynatrace to monitor your `checkout` service, databases, and hosts, and that metrics from all these entities use the tag `checkout-service` to denote requests coming from that service. By mapping the `checkout` service CI to the Dynatrace data tagged with `checkout-service`, Service Observability retrieves metrics for those databases and hosts and CIs related to the service, then displays them together. Operators can pinpoint issues on entities related to the service and narrow down the mitigation process without having to leave the SOW.

## Service Observability users

<table id="table_y3t_vym_rdc"><thead><tr><th>

User

</th><th>

Description

</th></tr></thead><tbody><tr><td>

System admin

</td><td>

Version 1.5 only.

 System admins configure users and teams, register services to be monitored, connect Service Observability to observability vendors, and then map those services to that data. They can also view the data in the SOW

</td></tr><tr><td>

Service Observability admin

</td><td>

Version 1.6.x and later.Service Observability admins can configure users and teams, connect Service Observability to observability vendors, and then map services to that data. They can also view the data in the SOW. Admins can also customize dashboard templates used to display metrics and related information.

</td></tr><tr><td>

Operator/operations manager**Note:** These users must belong to an `srm` group type to see all data.

</td><td>

Operators use Service Observability when triaging incidents in the SOW. They can view basic health metrics for a service, along with related incidents, alerts, and changes. They can get more detailed information by navigating to the **Observability** tab to view additional service metrics, along with metrics from related entities, such hosts, networks, or databases.

</td></tr></tbody>
</table>## Service Observability workflow

Admins configure Service Observability by creating a connection to an observability vendor and then mapping CI services to that data. Operators use Service Observability to determine if another related entity is causing issues surfaced by the service's performance.

As an admin, you:

1.  Determine the services to be monitored by Service Observability based on business criticality.
2.  Connect existing observability vendor instances to Service Observability.
3.  Map services to observability metric data using vendor-based tags attached to that data.
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

Consolidate data from existing monitoring tools, network health tools, cloud providers, ServiceNow agents, and third-party tools for a full-stack view of service health:-   Connect data from external Observability vendors.
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

Use generative AI to analyze metric data and find insights to help determine service health.

</td><td>

-   [Analyze a dashboard in Service Observability](../../now-assist-itom/concept/analyze-a-dashboard-in-service-observability.md)
-   [Analyze service health in Service Observability](../../now-assist-itom/concept/analyze-service-health-in-service-observability.md)

</td><td>

Operators

</td></tr><tr><td>

See Service Observability data as part of Incident Management workflows

</td><td>

[Digital End-User Experience and Service Observability UI experience on investigate tab](https://www.servicenow.com/docs/access?context=dex-so-metric-views-investigate-tab&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)

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

