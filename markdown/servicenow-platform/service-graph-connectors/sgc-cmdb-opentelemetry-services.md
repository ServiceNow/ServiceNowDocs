---
title: Linking inferred services with CIs
description: Create inferred services relationships in your ServiceNow instance with other Cloud Observability application services as originally configured in the application by linking an inferred service configuration item \(CI\) in CMDB with an inferred service from the Cloud Observability application.Link a Cloud Observability inferred service with a CI to create relationships between the inferred service and other Cloud Observability services in your ServiceNow instance.
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [OpenTelemetry, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Linking inferred services with CIs

Create inferred services relationships in your ServiceNow instance with other Cloud Observability application services as originally configured in the application by linking an inferred service configuration item \(CI\) in CMDB with an inferred service from the Cloud Observability application.

**Important:** Starting with the Australia release, Service Graph Connector for OpenTelemetry is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## Inferred services

The inferred services in the Cloud Observability application are referred to as external services, libraries, or dependencies such as a database or a third-party API that haven’t been instrumented with OpenTelemetry. These types of technologies are manually defined in the Cloud Observability application, and you can import them into your ServiceNow instance through the Service Graph Connector for OpenTelemetry.

For information about adding inferred services in the Cloud Observability application, see [Add inferred services](https://docs.lightstep.com/docs/inferred-services) in the Cloud Observability documentation.

## Storing inferred services data

The OpenTelemetry Dependency Map \[sn\_sg\_lightstep\_dependency\_map\] data source available with the Service Graph Connector for OpenTelemetry iterates through all the included projects in a Cloud Observability organization and pulls in the inferred services details. Inferred services details include mapping of related services. The data source saves these details in the Inferred service \[sn\_sg\_lightstep\_inferred\_service\] table.

The following attributes in the Inferred service \[sn\_sg\_lightstep\_inferred\_service\] table are populated by the OpenTelemetry Dependency Map \[sn\_sg\_lightstep\_dependency\_map\] data source.

|Attribute label|Attribute name|
|---------------|--------------|
|Project|project|
|Organization|organization|
|ID|id|
|Inferred service|inferred\_service|
|Inferred service CI|inferred\_service\_ci|
|Active|active|
|Last scan|last\_scan|
|Cloud Observability CI|cloud\_observability\_ci|

Due to insufficient information for defining identification rules, the pulled in inferred services don’t automatically bind to a CI in CMDB. However, as a user with the cmdb\_inst\_admin role, you can manually link a CI to an inferred service. The linking creates appropriate relationships with the related services and generates the inferred service mapping in the respective application service maps of your ServiceNow instance.

## Link an inferred service

Link a Cloud Observability inferred service with a CI to create relationships between the inferred service and other Cloud Observability services in your ServiceNow instance.

### Before you begin

**Important:** Starting with the Australia release, Service Graph Connector for OpenTelemetry is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Role required: cmdb\_inst\_admin

### Procedure

1.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **OpenTelemetry** &gt; **Inferred services**.

2.  Review the inferred services available from the Cloud Observability app in the **Inferred service** column.

3.  For an inferred service, double-click the **Inferred service CI** column cell.

4.  Select the lookup using list icon \(![Lookup using list icon.](../image/Lookup-list-icon.png)\) to search for and select an inferred service CI available within the Configuration item \[cmdb\_ci\] table.

5.  Select the save icon \(![Green check mark icon](../../../administer/workflow-administration/image/Check.png)\).

6.  Repeat the steps [3](sgc-cmdb-opentelemetry-services.md#select-ci) to [5](sgc-cmdb-opentelemetry-services.md#save-ci) for each inferred service that you want to link with a CI.


### Result

The **Update CI relationship** business rule is triggered that creates appropriate relationships for the inferred service with the related services and generates the inferred service mapping in the respective application service maps.

**Note:**

-   If you remove any mapping later, the **Delete CI relationship** business rule is triggered to delete any relationships between the inferred service CIs and the Cloud Observability inferred services.
-   For any inferred services that were not last scanned in the Cloud Observability app, the Service Graph Connector automatically deactivates the corresponding records in CMDB and deletes the relationship for the inactive records.

