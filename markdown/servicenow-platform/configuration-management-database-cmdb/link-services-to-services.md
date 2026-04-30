---
title: Link application services
description: You can manually link two application services by adding a reference to one application service into another application service. The service that contains the reference, becomes a dependent service. The service that you include as a reference is a contained service. You can link application services to create dependencies for impact monitoring in Event Management.
locale: en-US
release: yokohama
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Application services, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Link application services

You can manually link two application services by adding a reference to one application service into another application service. The service that contains the reference, becomes a dependent service. The service that you include as a reference is a contained service. You can link application services to create dependencies for impact monitoring in Event Management.

## Before you begin

You can edit discovered and manually created service instances.

**Important:** You cannot fine-tune or edit tag-based and dynamic services from the map.

Ensure that you know the name and the service type of the application service, to which you want to add a reference.

Role required: app\_service\_admin or service\_mapping\_admin

## About this task

To create a link, add a reference to the relevant application service as an outgoing connection of the relevant CI inside another application service. For example, you can add the UK Portal application service as a link to the Online Store application service. In this case, the Online Store service becomes dependent on the UK Portal service that it contains. The Online Store service reflects discovery errors for its contained service in the Edit map mode, as well as alerts in Event Management.

![Linked application service](../image/linked-services-dependent-contained.png "Example of linked application services")

When you link an application service to another application service, the information about the CI, to which you linked the service, is updated in the CMDB. The CMDB recognizes other application services that use the same applicative flow, and adds the contained application service to these application services by analogy. The same logic applies when you remove a contained application service: The system removes it from all application services where you either manually linked this service or the system linked this service by analogy.

When using Service Mapping, you may want to link application services to create:

-   A dependency between two application services.
-   A placeholder for a map branch that Service Mapping failed to discover. If you create or customize a pattern to discover the configuration item \(CI\) serving as an entry point for the contained service instance, Service Mapping can discover this contained service.
-   An indication that an service instance contains a branch, which Service Mapping cannot discover.

You can add an service instance as a contained service to as many service instance as necessary.

## Procedure

1.  Navigate to **Service Mapping** &gt; **Application Services**.

2.  Click **View map** next to the relevant application service.

3.  If needed, click **Edit** to ensure that the map is in Edit mode.

4.  Right-click the CI to which you want to link an application service as a reference.

5.  Select **Add A CI**.

6.  In the Add a CI dialog box, select the application service you want to add as a contained service:

<table id="table_pks_kwh_vcb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CI Type

</td><td>

Select the relevant service type from this list: -   `Tag-Based Application Service`
-   `Mapped Application Service` for discovered or manually created application services
-   `Calculated Application Service` for dynamic services
-   `Dynamic CI Group`


</td></tr><tr><td>

CI Name

</td><td>

Select the name of the application service that you want to link as a contained service.

</td></tr></tbody>
</table>7.  Click **Submit**.

    The icon for the contained service appears on the map.


**Related topics**  


[Application services](../../configuration-management/concept/application-services.md)

[View dependent application services in classic Service Mapping](https://www.servicenow.com/docs/access?context=view-linked-services&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)

[View contained application services in classic Service Mapping](https://www.servicenow.com/docs/access?context=view-contained-services&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)

