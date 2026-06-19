---
title: Service Observability data mapping form
description: Field descriptions for the Observability data mapping form. Use this form to map activated services in Service Observability to metrics from your observability instance. Each service can be mapped only once, but can contain exceptions to include all related entities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/service-observability/observability-data-mapping-form.html
release: australia
product: Service Observability
classification: service-observability
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service Observability reference, Service Observability, ITOM AIOps, IT Operations Management]
---

# Service Observability data mapping form

Field descriptions for the Observability data mapping form. Use this form to map activated services in Service Observability to metrics from your observability instance. Each service can be mapped only once, but can contain exceptions to include all related entities.

|Field|Description|
|-----|-----------|
|Mapping name|Name for the mapping. The name should be descriptive so that users understand where the data is coming from.|
|Services|Service to use for this mapping. Each service can be mapped only once.|
|**Default**|
|Find metrics from this source|Existing data connection to use for metrics. To add a connection, see [Connect a Service Observability data source](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-observability/connect-an-observability-data-source.md).|
|where source tag key|Tag key that you want to map to the activated service. If you use more than one tag to represent a service, you can create an exception. For example, most tags use `service_name` except for database metrics, which use `service`.|
|source tag value|Value that represents the service name. Values can be strings or a variable that represents fields on the CI for the service. You can use variables on your observability data as the value to map multiple entities at once. For example, if your observability data uses the `$service_name` variable and you enter that as the **source tag value**, all services using that value are mapped.|
|**Exceptions**|
|For entity type|Entity that uses a different key or value than the default.|
|Find metrics from this source|Existing data connection to use for metrics. To add a connection, see [Connect a Service Observability data source](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-observability/connect-an-observability-data-source.md).|
|where source tag key|Tag key that you want to map to the activated service for this entity.|
|source tag value|Value that represents the service name. Values can be strings or a variable that represents fields on the CI for the service.|

**Parent Topic:**[Service Observability reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-observability/service-observability-reference.md)

