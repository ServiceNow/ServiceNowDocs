---
title: Service Graph Connector for OpenTelemetry
description: Use the Service Graph Connector for OpenTelemetry to ingest Configuration Management Database \(CMDB\) data from the ServiceNow Cloud Observability \(formerly Lightstep\) application using REST APIs. Push events from the Cloud Observability application into ServiceNow with Event Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-graph-connectors/sgc-cmdb-integration-opentelemetry.html
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for OpenTelemetry

Use the Service Graph Connector for OpenTelemetry to ingest Configuration Management Database \(CMDB\) data from the ServiceNow Cloud Observability \(formerly Lightstep\) application using REST APIs. Push events from the Cloud Observability application into ServiceNow with Event Management.

**Important:** Starting with the Australia release, Service Graph Connector for OpenTelemetry is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Supported ServiceNow versions

-   Utah
-   Vancouver
-   Washington DC

## Use cases

The following examples describe how you can use the Service Graph Connector for OpenTelemetry:

-   Import project topologies from Cloud Observability so that the site reliability engineering \(SRE\) teams can have a single view for triage with other ServiceNow data points \(such as a change request, an incident\) from a single view.
-   Import events created by Cloud Observability against monitored projects to pinpoint SRE triage activities.

## Guided setup

The guided setup for the Service Graph Connector for OpenTelemetry provides an organized sequence of tasks to configure the integration on your instance. To access the guided setup, see [Configure Service Graph Connector for OpenTelemetry](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-config-opentelemetry-integ.md).

## CMDB integrations dashboard

The Integration Commons for CMDB store app provides a dashboard with a central view of the status, processing results, and processing errors of all installed integrations. You can see metrics for all integration runs. You can filter the view to a specific CMDB integration, a specific time duration, or a specific integration run. For more details about monitoring Cloud Observability integrations in the CMDB Integrations Dashboard, see [Using the CMDB Integrations Dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/cmdb-integration-commons/integration-commons-for-cmdb.md).

## Data mapping

Data from the Cloud Observability data sources is mapped and transformed into the ServiceNow CMDB configuration item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the ServiceNow CMDB using the Identification and Reconciliation Engine \(IRE\).

When you complete setting up the connection, you can configure the integration to pull data from the application periodically.

The following table describes the data sources, the scheduled jobs, the staging tables, and the target tables as CMDB CI classes for the Cloud Observability application.

<table id="table_udz_pgq_1bc" class="custom-rows"><thead><tr><th class="filter">

Data source

</th><th>

Description

</th><th>

Scheduled job

</th><th>

Staging table

</th><th>

CMDB CI classes

</th></tr></thead><tbody><tr><td>

OpenTelemetry Resources

</td><td>

Imports all the Kubernetes clusters, workloads, and application services from the OpenTelemetry traces.

</td><td>

OpenTelemetry ResourcesOpenTelemetry Delta Resources

</td><td>

OpenTelemetry Resources \[sn\_sg\_lightstep\_resources\]

</td><td>

[Calculated Application Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-opentelemetry-classes.md)

 [Kubernetes Cluster](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-opentelemetry-classes.md)

 [Kubernetes Deployment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-opentelemetry-classes.md)

 [Kubernetes Node](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-opentelemetry-classes.md)

 [Kubernetes Pod](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-opentelemetry-classes.md)

 [Kubernetes StatefulSet](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-opentelemetry-classes.md)

 [Kubernetes ReplicaSet](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-opentelemetry-classes.md)

 [Kubernetes DaemonSet](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-opentelemetry-classes.md)

 [Kubernetes Job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-opentelemetry-classes.md)

 [Kubernetes Cronjob](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-opentelemetry-classes.md)

 [Kubernetes Namespace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-opentelemetry-classes.md)

 [Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-opentelemetry-classes.md)

 [Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-opentelemetry-classes.md)

</td></tr><tr><td>

OpenTelemetry Pods

</td><td>

Imports all the Kubernetes pods from the containers.

</td><td>

OpenTelemetry PodsOpenTelemetry Delta Pods

</td><td>

OpenTelemetry K8s Pods \[sn\_sg\_lightstep\_pods\]

</td><td>

[Kubernetes Cluster](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-opentelemetry-classes.md)

 [Kubernetes Pod](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-opentelemetry-classes.md)

</td></tr><tr><td>

OpenTelemetry Containers

</td><td>

Imports all the containers from the OpenTelemetry traces.

</td><td>

OpenTelemetry ContainersOpenTelemetry Delta Containers

</td><td>

OpenTelemetry docker containers \[sn\_sg\_lightstep\_containers\]

</td><td>

[Docker Container](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-opentelemetry-classes.md)

</td></tr><tr><td>

OpenTelemetry Container Images

</td><td>

Imports all the container images from the OpenTelemetry traces.

</td><td>

OpenTelemetry Container ImagesOpenTelemetry Delta Container Images

</td><td>

Opentelemetry container images \[sn\_sg\_lightstep\_container\_images\]

</td><td>

[Docker Image](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-opentelemetry-classes.md)

</td></tr><tr><td>

OpenTelemetry Services

</td><td>

Imports all the Kubernetes services from the OpenTelemetry traces.

</td><td>

OpenTelemetry Delta ServicesOpenTelemetry Services

</td><td>

OpenTelemetry K8s Services \[sn\_sg\_lightstep\_kubernetes\_services\]

</td><td>

[Kubernetes Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-opentelemetry-classes.md)

</td></tr><tr><td>

OpenTelemetry Dependency Map

</td><td>

Imports the dependency maps to get an aggregate view of the traced data.The data source also imports and loads any inferred services and their related services data in the Inferred service \[sn\_sg\_lightstep\_inferred\_service\] staging table.

**Note:** You need to link the imported inferred services with a CI manually. See [Inferred service linking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-integration-opentelemetry.md).

</td><td>

OpenTelemetry Dependency Map

</td><td>

OpenTelemetry Dependency Map \[sn\_sg\_lightstep\_dependency\_map\]

</td><td>

[Calculated Application Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-opentelemetry-classes.md)

</td></tr></tbody>
</table>For more information on where data is saved when pulling data from Cloud Observability, see [CMDB classes targeted in Service Graph Connector for OpenTelemetry](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-opentelemetry-classes.md).

You can use the IntegrationHub ETL app to view the data maps. See [IntegrationHub ETL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/integration-hub-etl/integrationhub-etl.md) for more information.

## Inferred service linking

The ServiceNow Cloud Observability application can infer the presence of an inferred service when the span calling the remote service has the necessary information. Service Graph Connector for OpenTelemetry provides the linking of inferred services and their related services with CIs in the CMDB. For more information, see [Linking inferred services with CIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-opentelemetry-services.md).

**Related topics**  


[Service Graph Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-sgc-available.md)

