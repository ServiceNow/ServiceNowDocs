---
title: Observability vendor entity mappings for Service Observability
description: Understand how Service Observability maps service, host, and database entities to your observability vendor resources.
locale: en-US
release: zurich
product: Service Observability
classification: service-observability
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Service Observability reference, Service Observability, ITOM AIOps, IT Operations Management]
---

# Observability vendor entity mappings for Service Observability

Understand how Service Observability maps service, host, and database entities to your observability vendor resources.

Service Observability displays metrics from your observability vendor for services, hosts, databases, and network components on the Observability dashboards based on the key:value pairs in the [mapping rules you create](../task/create-and-manage-observability-data-mappings.md) during configuration. Service Observability sends a request to the observability vendor using that mapping as a filter to find related entities. Any additional filtering needed to find the entities is noted in the following sections.

## Amazon CloudWatch entity mapping

Resources are returned using the AWS `GetResources` API.

|Service Observability entity category|Service Observability entity dashboard|AWS resource|
|-------------------------------------|--------------------------------------|------------|
|**Application**|API Gateway - HTTP|API Gateway HTTP APIs|
| |API Gateway - REST|API Gateway REST APIs|
| |ELB|ELB application load balancers|
| |Lambda|Lambda functions|
|**Compute**|Host|EC2 instances|
|**Databases**|RDS|RDS database instances|

## AppDynamics entity mapping

Resources are returned using the value of the `entityName` property.

|Service Observability entity category|Service Observability entity dashboard|AppDynamics resource|
|-------------------------------------|--------------------------------------|--------------------|
|**Application**|Service|AppDynamics applications returned by the `/controller/rest/applications/` API|
|**Compute**|Host|Server nodes for applications returned by the `/controller/sim/v2/user/machines/keys/` API|
|**Databases**|MySQL|MySQL database instances returned by the `/controller/rest/databases/collectors/`|
| |PostgreSQL|MySQL database instances returned by the `/controller/rest/databases/collectors/`|

## Azure entity mapping

Resources are returned using the Azure `ResourceGraph` API.

<table id="table_wzg_sff_yfc"><thead><tr><th>

Service Observability entity category

</th><th>

Service Observability entity dashboard

</th><th>

Azure resource

</th></tr></thead><tbody><tr><td>

**Application**

</td><td>

Service

</td><td>

-   `Microsoft.Compute/cloudServices`

-   `Microsoft.Web/sites`

</td></tr><tr><td>

**Compute**

</td><td>

Host

</td><td>

`Microsoft.Compute/virtualMachines`

</td></tr><tr><td>

**Databases**

</td><td>

MySQL

</td><td>

-   `Microsoft.DBforMySQL/servers`

-   `Microsoft.DBforMySQL/flexibleServers`


</td></tr><tr><td>

 

</td><td>

PostgreSQL

</td><td>

-   `Microsoft.DBforPostgreSQL/servers`

-   `Microsoft.DBforPostgreSQL/flexibleServers`


</td></tr></tbody>
</table>## Datadog entity mapping

<table id="table_cnw_jkf_yfc"><thead><tr><th>

Service Observability entity category

</th><th>

Service Observability entity dashboard

</th><th>

Datadog resource

</th></tr></thead><tbody><tr><td>

**Application**

</td><td>

Service

</td><td>

Entities returned from the Software Catalog: List Entities API

</td></tr><tr><td>

**Compute**

</td><td>

Host

</td><td>

Hosts returned from the Hosts: List Hosts API

</td></tr><tr><td>

**Databases**

</td><td>

MySQL

</td><td>

Databases returned by filtering the `mysql.net.max_connections` metric, filtered by the provided key:value pair in the data mapping.**Note:** If your databases don't emit this metric, they aren't mapped.

</td></tr><tr><td>

 

</td><td>

PostgreSQL

</td><td>

Databases returned by filtering the `postgresql.connections` metric, filtered by the provided key:value pair in the data mapping.**Note:** If your databases don't emit this metric, they aren't mapped.

</td></tr></tbody>
</table>Items of note:

-   Service entities: The `Software Catalog list entities` API only returns data for services that include metadata. If you want to map services that don't include metadata, you must create a mapping using `service` as the tag and the name of the service as the value.

    For example, say you have a service named `internet-banking-4` that you want to use in a mapping and it doesn't contain metadata. You set up the mapping as shown in this screenshot.

    ![How to map a service that doesn't contain metadata](../image/so_dd_mapping.png "Datadog mapping if no metadata is present")

-   Default dashboard templates: The Requests, Errors, and Latency charts on the Overview and Observability dashboard templates are created using the Datadog `trace.http.request` trace metric. If a service isn't emitting that metric, no data is found. You can customize the template to use a different trace metric query. See [Customize Service Observability dashboard templates](../task/customize-service-observability-dashboard-templates.md) for more information.

## Dynatrace entity mapping

You can use either the Dynatrace Classic query or Grail \(DQL\) query, however both require separate data connections. For Grail queries, Service Observability first queries the Grail data source and if not found, will fall back to a Classic query.

|Service Observability entity category|Service Observability entity dashboard|Dynatrace resource|
|-------------------------------------|--------------------------------------|------------------|
|**Application**|Service|Services|
|**Compute**|Host|Hosts|
|**Databases**|MySQL|MySQL database instances|
| |PostgreSQL|PostgreSQL database instances|

## New Relic entity mapping

|Service Observability entity category|Service Observability entity dashboard|New Relic resource|
|-------------------------------------|--------------------------------------|------------------|
|**Application**|Service|Application services|
|**Compute**|Host|Hosts|
|**Databases**|MySQL|MySQL database instances|
| |PostgreSQL|PostgreSQL database instances|

## Prometheus entity mapping

|Service Observability entity category|Service Observability entity dashboard|Prometheus resource|
|-------------------------------------|--------------------------------------|-------------------|
|**Application**|Service|Applications|
|**Compute**|Host|Server nodes for applications|
|**Databases**|MySQL|MySQL database instances|
| |PostgreSQL|PostgreSQL database instances|

## SolarWinds entity mapping

<table id="table_tvq_kkf_yfc"><thead><tr><th>

Service Observability entity category

</th><th>

Service Observability entity dashboard

</th><th>

SolarWinds resource

</th></tr></thead><tbody><tr><td>

**Application**

</td><td>

Service

</td><td>

Application services

</td></tr><tr><td>

**Compute**

</td><td>

Host

</td><td>

Hosts

</td></tr><tr><td>

**Networking**

</td><td>

Firewall

</td><td>

By default, data mappings find and display metrics using Palo Alto Firewall keys.If you want metrics from a different firewall, follow the instructions for [customizing dashboard templates](../task/customize-service-observability-dashboard-templates.md).

</td></tr><tr><td>

 

</td><td>

Load Balancer

</td><td>

By default, data mappings find and display metrics using F5 Big-IP Load Balancer keys.If you want metrics from a different load balancer, follow the instructions for [customizing dashboard templates](../task/customize-service-observability-dashboard-templates.md).

</td></tr><tr><td>

 

</td><td>

Interface

</td><td>

Network interfaces

</td></tr><tr><td>

 

</td><td>

Other Network Devices

</td><td>

Other network devices, such as switches and routers

</td></tr></tbody>
</table>Items to note:

-   You can use custom properties for key/value pairs in a data mapping.
-   If you are using SolarWinds as an exception in your mapping to ingest networking metrics, using custom properties is optional. If you do use them, only entities with those properties in their metadata are returned. If you leave the tag and key values blank, all supported entities are returned.

## Splunk entity mapping

Resources are returned using the Splunk Metric time series Metadata API. Service Observability searches for matching key:value pairs in custom properties and then falls back to searching dimensions.

The returned payload is then filtered by the presence of a specific metric in the metadata that corresponds with an entity type.

<table id="table_x1w_kkf_yfc"><thead><tr><th>

Service Observability entity category

</th><th>

Service Observability entity dashboard

</th><th>

Splunk Property or dimension

</th><th>

Splunk metric used for filtering

</th></tr></thead><tbody><tr><td>

**Application**

</td><td>

Service

</td><td>

-   Property: `sf_service`

-   Dimension fallback: `service.name`


</td><td>

`sf_metric:service.request`

</td></tr><tr><td>

**Compute**

</td><td>

Host

</td><td>

-   Property: `host.name`

-   Dimension fallback: `host.id`


</td><td>

`sf_metric:disk.summary_utilization`

</td></tr><tr><td>

**Databases**

</td><td>

MySQL

</td><td>

-   Property: `mysql.instance.name`

-   Dimension fallback: `mysql.instance.endpoint`


</td><td>

`sf_metric:mysql.threads`

</td></tr><tr><td>

 

</td><td>

PostgreSQL

</td><td>

Not supported

</td><td>

 

</td></tr></tbody>
</table>## Zabbix entity mapping

In Zabbix, every monitored entity is categorized as a host. To enable differentiation between entities, Service Observability searches for keywords in attributes on metadata tags, including host tags, inherited tags, templates, and host groups. Any Zabbix host that does not match a keyword are classified and displayed as Host entities.

The following table shows the keywords used to find distinct entities. Keywords are case insensitive.

<table id="table_l1n_xzr_23c"><thead><tr><th>

Service Observability entity category

</th><th>

Service Observability entity dashboard

</th><th>

Metadata keyword

</th></tr></thead><tbody><tr><td>

**Application**

</td><td>

Service

</td><td>

-   Apache
-   nginx
-   Kubernetes
-   cluster
-   application

</td></tr><tr><td>

**Compute**

</td><td>

Host

</td><td>

Any non-matching keyword

</td></tr><tr><td>

**Databases**

</td><td>

MySQL

</td><td>

-   Mysql
-   Msql
-   mariadb

</td></tr><tr><td>

 

</td><td>

PostgreSQL

</td><td>

-   Postgres
-   Psql
-   Pgsql
-   Postgresql

</td></tr><tr><td>

**Networking**

</td><td>

Firewall

</td><td>

-   Firewall
-   palo-alto
-   palo alto
-   pan
-   fortigate
-   fortinet
-   fgt
-   sophos
-   sonicwall
-   watchguard
-   zscaler

By default, data mappings find and display metrics using Palo Alto Firewall keys.If you want metrics from a different firewall, follow the instructions for [customizing dashboard templates](../task/customize-service-observability-dashboard-templates.md).

</td></tr><tr><td>

 

</td><td>

Load Balancer

</td><td>

-   Loadbalancer
-   load\_balancer
-   alb
-   nlb
-   f5
-   netscaler
-   big-ip
-   bigip

By default, data mappings find and display metrics using F5 Big-IP Load Balancer keys.If you want metrics from a different load balancer, follow the instructions for [customizing dashboard templates](../task/customize-service-observability-dashboard-templates.md).

</td></tr><tr><td>

 

</td><td>

Other Network devices

</td><td>

-   Network
-   router
-   rt
-   gateway
-   gw
-   juniper
-   junos
-   switch
-   catalyst
-   nexus
-   arista

</td></tr><tr><td>

 

</td><td>

 

</td><td>

 

</td></tr></tbody>
</table>Item to note:

The default dashboards for each entity type display metrics using Zabbix standard keys. If your implementation uses custom item keys, you need to [customize your dashboard templates](../task/customize-service-observability-dashboard-templates.md) accordingly.

**Parent Topic:**[Service Observability reference](service-observability-reference.md)

