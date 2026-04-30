---
title: Service Graph Connector for OpenTelemetry
description: Use the Service Graph Connector for OpenTelemetry to ingest Configuration Management Database \(CMDB\) data from the ServiceNow Cloud Observability \(formerly Lightstep\) application using REST APIs. Push events from the Cloud Observability application into ServiceNow with Event Management.
locale: en-US
release: xanadu
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2026-02-27"
reading_time_minutes: 4
breadcrumb: [Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for OpenTelemetry

Use the Service Graph Connector for OpenTelemetry to ingest Configuration Management Database \(CMDB\) data from the ServiceNow Cloud Observability \(formerly Lightstep\) application using REST APIs. Push events from the Cloud Observability application into ServiceNow with Event Management.

**Important:** Starting with the Australia release, Service Graph Connector for OpenTelemetry is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Supported ServiceNow versions

-   Utah
-   Vancouver
-   Washington DC

## Use cases

The following examples describe how you can use the Service Graph Connector for OpenTelemetry:

-   Import project topologies from Cloud Observability so that the site reliability engineering \(SRE\) teams can have a single view for triage with other ServiceNow data points \(such as a change request, an incident\) from a single view.
-   Import events created by Cloud Observability against monitored projects to pinpoint SRE triage activities.

## Guided setup

The guided setup for the Service Graph Connector for OpenTelemetry provides an organized sequence of tasks to configure the integration on your instance. To access the guided setup, see [Configure Service Graph Connector for OpenTelemetry](../task/sgc-config-opentelemetry-integ.md).

## CMDB integrations dashboard

The Integration Commons for CMDB store app provides a dashboard with a central view of the status, processing results, and processing errors of all installed integrations. You can see metrics for all integration runs. You can filter the view to a specific CMDB integration, a specific time duration, or a specific integration run. For more details about monitoring Cloud Observability integrations in the CMDB Integrations Dashboard, see [Using the CMDB Integrations Dashboard](integration-commons-for-cmdb.md#section_fxg_lh4_blb).

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

[Calculated Application Service](../reference/sgc-cmdb-opentelemetry-classes.md#section_fr5_b3g_fxb)

 [Kubernetes Cluster](../reference/sgc-cmdb-opentelemetry-classes.md#section_xzj_khg_fxb)

 [Kubernetes Deployment](../reference/sgc-cmdb-opentelemetry-classes.md#section_hyk_1hg_fxb)

 [Kubernetes Node](../reference/sgc-cmdb-opentelemetry-classes.md#section_vf1_dhg_fxb)

 [Kubernetes Pod](../reference/sgc-cmdb-opentelemetry-classes.md#section_rkm_1kg_fxb)

 [Kubernetes StatefulSet](../reference/sgc-cmdb-opentelemetry-classes.md#section_hg4_fl5_qxb)

 [Kubernetes ReplicaSet](../reference/sgc-cmdb-opentelemetry-classes.md#section_zdf_phg_fxb)

 [Kubernetes DaemonSet](../reference/sgc-cmdb-opentelemetry-classes.md#section_q2s_5hg_fxb)

 [Kubernetes Job](../reference/sgc-cmdb-opentelemetry-classes.md#section_u1r_gdb_rxb)

 [Kubernetes Cronjob](../reference/sgc-cmdb-opentelemetry-classes.md#section_jls_jcb_rxb)

 [Kubernetes Namespace](../reference/sgc-cmdb-opentelemetry-classes.md#section_gz4_lhg_fxb)

 [Server](../reference/sgc-cmdb-opentelemetry-classes.md#section_y5x_yhg_fxb)

 [Key Value](../reference/sgc-cmdb-opentelemetry-classes.md#section_hbk_fhg_fxb)

</td></tr><tr><td>

OpenTelemetry Pods

</td><td>

Imports all the Kubernetes pods from the containers.

</td><td>

OpenTelemetry PodsOpenTelemetry Delta Pods

</td><td>

OpenTelemetry K8s Pods \[sn\_sg\_lightstep\_pods\]

</td><td>

[Kubernetes Cluster](../reference/sgc-cmdb-opentelemetry-classes.md#section_xzj_khg_fxb)

 [Kubernetes Pod](../reference/sgc-cmdb-opentelemetry-classes.md#section_rkm_1kg_fxb)

</td></tr><tr><td>

OpenTelemetry Containers

</td><td>

Imports all the containers from the OpenTelemetry traces.

</td><td>

OpenTelemetry ContainersOpenTelemetry Delta Containers

</td><td>

OpenTelemetry docker containers \[sn\_sg\_lightstep\_containers\]

</td><td>

[Docker Container](../reference/sgc-cmdb-opentelemetry-classes.md#section_vx1_thg_fxb)

</td></tr><tr><td>

OpenTelemetry Container Images

</td><td>

Imports all the container images from the OpenTelemetry traces.

</td><td>

OpenTelemetry Container ImagesOpenTelemetry Delta Container Images

</td><td>

Opentelemetry container images \[sn\_sg\_lightstep\_container\_images\]

</td><td>

[Docker Image](../reference/sgc-cmdb-opentelemetry-classes.md#section_vyl_d3g_fxb)

</td></tr><tr><td>

OpenTelemetry Services

</td><td>

Imports all the Kubernetes services from the OpenTelemetry traces.

</td><td>

OpenTelemetry Delta ServicesOpenTelemetry Services

</td><td>

OpenTelemetry K8s Services \[sn\_sg\_lightstep\_kubernetes\_services\]

</td><td>

[Kubernetes Service](../reference/sgc-cmdb-opentelemetry-classes.md#section_kgl_mhg_fxb)

</td></tr><tr><td>

OpenTelemetry Dependency Map

</td><td>

Imports the dependency maps to get an aggregate view of the traced data.The data source also imports and loads any inferred services and their related services data in the Inferred service \[sn\_sg\_lightstep\_inferred\_service\] staging table.

**Note:** You need to link the imported inferred services with a CI manually. See [Inferred service linking](sgc-cmdb-integration-opentelemetry.md#section_h12_fwb_sxb).

</td><td>

OpenTelemetry Dependency Map

</td><td>

OpenTelemetry Dependency Map \[sn\_sg\_lightstep\_dependency\_map\]

</td><td>

[Calculated Application Service](../reference/sgc-cmdb-opentelemetry-classes.md#section_fr5_b3g_fxb)

</td></tr></tbody>
</table>For more information on where data is saved when pulling data from Cloud Observability, see [CMDB classes targeted in Service Graph Connector for OpenTelemetry](../reference/sgc-cmdb-opentelemetry-classes.md).

You can use the IntegrationHub ETL app to view the data maps. See [IntegrationHub ETL](integrationhub-etl.md) for more information.

## Inferred service linking

The ServiceNow Cloud Observability application can infer the presence of an inferred service when the span calling the remote service has the necessary information. Service Graph Connector for OpenTelemetry provides the linking of inferred services and their related services with CIs in the CMDB. For more information, see [Linking inferred services with CIs](sgc-cmdb-opentelemetry-services.md#).

**Related topics**  


[Service Graph Connectors](cmdb-sgc-available.md)

