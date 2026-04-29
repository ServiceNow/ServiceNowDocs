---
title: Service Observability data mapping form
description: Field descriptions for the Observability data mapping form. Use this form to map activated services in Service Observability to metrics from your observability instance. Each service can be mapped only once, but can contain exceptions to include all related entities.
locale: en-US
release: australia
product: Service Observability
classification: service-observability
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Service Observability reference, Service Observability, ITOM AIOps, IT Operations Management]
---

# Service Observability data mapping form

Field descriptions for the Observability data mapping form. Use this form to map activated services in Service Observability to metrics from your observability instance. Each service can be mapped only once, but can contain exceptions to include all related entities.

<table id="table_jkt_gvj_xdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Mapping name

</td><td>

Name for the mapping. The name should be descriptive so that users understand where the data is coming from.

</td></tr><tr><td>

Services

</td><td>

Service to use for this mapping. Each service can be mapped only once. For version 1.5.0 of Service Observability, services must be activated to be mapped. To activate a service, see [Activate teams and services](../concept/activate-teams-and-services.md).

</td></tr><tr><td colspan="2">

**Default**

</td></tr><tr><td>

Find metrics from this source

</td><td>

Existing data connection to use for metrics. To add a connection, see [Connect a Service Observability data source](../task/connect-an-observability-data-source.md).

</td></tr><tr><td>

where source tag key

</td><td>

Tag key that you want to map to the activated service. If you use more than one tag to represent a service, you can create an exception. For example, most tags use `service_name` except for database metrics, which use `service`.

</td></tr><tr><td>

source tag value

</td><td>

Value that represents the service name. Values can be strings or a variable that represents fields on the CI for the service. You can use variables on your observability data as the value to map multiple entities at once. For example, if your observability data uses the `$service_name` variable and you enter that as the **source tag value**, all services using that value are mapped.

</td></tr><tr><td colspan="2">

**Exceptions**

</td></tr><tr><td>

For entity type

</td><td>

Entity that uses a different key or value than the default.

</td></tr><tr><td>

Find metrics from this source

</td><td>

Existing data connection to use for metrics. To add a connection, see [Connect a Service Observability data source](../task/connect-an-observability-data-source.md).

</td></tr><tr><td>

where source tag key

</td><td>

Tag key that you want to map to the activated service for this entity.

</td></tr><tr><td>

source tag value

</td><td>

Value that represents the service name. Values can be strings or a variable that represents fields on the CI for the service.

</td></tr></tbody>
</table>**Parent Topic:**[Service Observability reference](service-observability-reference.md)

