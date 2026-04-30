---
title: Map a single application service using classic Service Mapping
description: In addition to mapping application services in bulk, you can map individual, single application services by defining attributes for each application service. Use this mapping method if you already know or are planning to find out application service details. You must have Service Mapping enabled to map or review application services.
locale: en-US
release: xanadu
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 11
breadcrumb: [Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Map a single application service using classic Service Mapping

In addition to mapping application services in bulk, you can map individual, single application services by defining attributes for each application service. Use this mapping method if you already know or are planning to find out application service details. You must have Service Mapping enabled to map or review application services.

## Before you begin

-   [Verify that Service Mapping is set up properly](check-service-mapping-readiness-for-mapping.md).
-   If the service instance relies on PaaS supported by Microsoft Azure or Amazon Web Services, [discover datacenters](../../discovery/concept/discovery-manager.md#) and then create [horizontal discovery schedules](../../discovery/concept/discovery-manager.md#) on the cloud service account.

Role required: service\_mapping\_admin

## About this task

You can map single application services in addition to bulk mapping, which is effective at mapping multiple application services, but is not precise. You may need to individually map application services omitted during bulk mapping.

The most important attribute you must know and configure to discover an application service is an entry point.

An entry point is a point where clients access a service instance. Usually, it is either a URL or a combination of the IP address and port. Service Mapping starts the mapping process from this point. For example, to map your electronic mailing application service, define an IP address or host name of the email server as an entry point.

Entry points vary depending on the nature of the service instance. Service Mapping comes with a wide range of preconfigured entry point types that cover many commonly used applications.

In addition to entry points that Service Mapping can discover, you may add entry points that Service Mapping cannot discover. You may want to add such an entry point as an indication that your service instance contains a device or application.

Also, you must define an owner for your service instance. The service instance owner is a user who is familiar with the infrastructure and applications making up the service. This user is the service instance SME who provides information necessary for a successful creation of a service instance. After a service is mapped, this user reviews the results, and either approves it or suggests changes.

After Service Mapping discovers configuration items \(CIs\) belonging to your application service for the first time, it then rediscovers CIs to find changes and updates. Create or modify discovery schedules to control how often Service Mapping rediscovers services or CIs.

All application services, both manually created and discovered by Service Mapping, are stored in the Mapped Application Service \[cmdb\_ci\_service\_discovered\] table.

You can also create a single application service manually using the flow based on Common Service Data Model. The Common Service Data Model \(CSDM\) helps you streamline service types and service offerings. You can add relationships between application services and other service-related objects in the CSDM: Business Application, Technical Service Offerings, or Business Service Offerings. For more information, see [Create application services](https://www.servicenow.com/docs/access?context=create-it-services&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) .

## Procedure

1.  Navigate to **All** &gt; **Service Mapping** &gt; **Home**.

    The Home page displays only information on service instances that Service Mapping can discover or already discovered. The Home page does not display information on service instances that are created manually or using the API.

2.  Click **Additional options** under the **Map** tile.

3.  Click **Define A Single Service Map**.

4.  Define the basic service instance attributes:

<table id="table_wvm_h2p_ls"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a unique application service name which is not in use by any other type of application service. Use self-explanatory names such as`mailing service` or `printing service`.

</td></tr><tr><td>

Owner

</td><td>

Select an owner who is responsible for this application service in the organization. If the owner name does not appear in the list, create a user for this person and assign the sm\_app\_owner role to this user. Alternatively, choose a user with the service\_mapping\_admin role.

</td></tr></tbody>
</table>5.  If you do not know the entry points, request them from the service instance owner, as described in [Request information about entry points for application services](request-info-entry-points.md).

6.  To add an entry point that Service Mapping can discover, perform these steps.

    1.  Click **Discoverable by Service Mapping**.

        The page offers tiles for applications most commonly used for entry points.

    2.  Click the tile matching the application to which the entry point belongs.

        For example, **Web Application** if you create an service instance with a web interface. If the tiles do not contain the necessary application, click **See More Types** to choose from a list of all preconfigured entry point types.

        **Important:** Do not use central IT components like Microsoft MQ or Microsoft Active Directory as entry points. Using such entry points creates large services, which cause performance issues during mapping and monitoring.

    3.  If the required entry point type does not appear in the list, you may need to create it as described in [Create entry point types for Service Mapping](t_CreateEntryPoint.md).

    4.  Configure attributes for the entry point as described in [Entry point attributes](../reference/r_EntryPointsforBizSvcDef.md).

        Entry point attributes depend on the type you select.

    5.  Click **Add**.

        The entry point is added under **Entry Points**.

    6.  To add more entry points, click **Add Entry Point** and repeat step [6](t_DefineNewBusinessService.md#step_defineentrypoint).

7.  To add a static entry point that Service Mapping cannot discover, perform these steps.

    1.  Click **Manually created**.

    2.  Define the CI to serve as the entry point.

<table id="table_ks2_1kr_31b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CI Type

</td><td>

Select the CI type \(CI class\) for the CI you are adding. Every CI belongs to a CI type which contains a set of attributes configured for this kind of CI, for example, **cmdb\_ci\_appl** for applications.

</td></tr><tr><td>

CI Name

</td><td>

Select the CI from the list of CIs of the selected CI type.**Note:** To eliminate the possibility of delayed results when searching for a specific CI, make your search as specific as possible. A search with \*&lt;name&gt; might take a long time and return a large data set.

</td></tr></tbody>
</table>        The CI type list includes only allowed CI types. For example, you cannot add an application cluster.

    3.  Click **Submit**.

8.  To save attributes you have defined up until this moment and carry on configuring attributes for this service instance, click **Save** or **Update**.

    Service Mapping saves the new service instance in the Mapped Application Service \[cmdb\_ci\_service\_discovered\] table. It also starts the discovery process in the background.

9.  To save definitions, discover this service instance, and navigate to the map for this service instance, click **View Map**.

    Service Mapping starts the discovery process. The map for this service instance page opens and displays the mapping in progress. The service instance status changes to In Progress.


## What to do next

-   If Service Mapping discovers the service instance with errors, [fix errors in individual application services using discovery messages](fix-errors-by-discovery-messages.md).
-   Make sure that the application services aren't too large:

    -   Service Mapping doesn't offer to view CI list instead of a map for a service instance.
    -   There is no discovery message indicating that the application service is too large: **The map does not display the entire service, because it is too large. The number of CI connections exceeded the allowed maximum.**
    If some application services are too large, resolve the service size issue:

    -   If you use customized discovery patterns and mapping results in very large application services, modify the patterns so that they don't map irrelevant CIs.
    -   [Split the service into smaller services](add-segment-to-business-service-map.md).
-   Send application services discovered without errors to their respective owners for approval. For more information, see [Send application service maps for review](send-business-service-for-review.md).

-   **[Request information about entry points for application services](request-info-entry-points.md)**  
The most important attribute you must know and configure to discover an service instance is an entry point. If you do not know the entry points for the service instance, request this information from the service instance owner.
-   **[Provide entry points for mapping an application service](provide-entry-point-info-owner.md)**  
As an application service owner you may receive a request for information about entry points in an email notification. Provide information about entry points to enable administrators to start discovery of an application service.
-   **[Add or remove CIs for single application services using connection suggestions](add-remove-ci-connections-services.md)**  
If discovery based on Predictive Intelligence is enabled, newly mapped application services include only configuration items \(CIs\) and CI connections added using discovery patterns. Use the suggestions for CI connections, generated by Service Mapping, to complete the application service.
-   **[Add CIs for single application services using connection rules](add-cis-connection-rules-single.md)**  
Create rules for automatically adding traffic-based connections and the CIs they lead to in discovered application services. Add CIs to specific application services using connection rules.
-   **[Enable traffic-based discovery for an application service](enable-traffic-based-discovery-business-service.md)**  
Make Service Mapping use traffic-based connections to discover CIs making up an application service.
-   **[Mapping application services containing Citrix XenApp and Presentation Server](../concept/mapping-services-citrix.md#)**  
Service Mapping can discover application services containing Citrix XenApp, Presentation Server, and Citrix Usage Collector.
-   **[Mapping application services containing Microsoft Exchange Server](../concept/mapping-service-exchange.md#)**  
Service Mapping can discover service instances containing a Microsoft Exchange Server and the Exchange Server components.
-   **[Tibco BusinessWorks and EMS discovery](../concept/mapping-services-tibco.md#)**  
Discovery can find Tibco ActiveMatrix BusinessWorks and Enterprise Message Service \(EMS\). Service Mapping can discover application services containing Tibco BusinessWorks, Enterprise Message Service \(EMS\), and their components.
-   **[Mapping application services containing Oracle GlassFish Servers](../concept/mapping-services-glassfish.md#)**  
Service Mapping can discover application services containing Oracle GlassFish Servers.
-   **[Mapping application services containing Oracle Tuxedo platform](../concept/mapping-services-tuxedo.md#)**  
Service Mapping can discover application services containing Oracle Tuxedo platform and its components.

**Parent Topic:**[Application service mapping using classic Service Mapping](../concept/c_DefineMapBusinessServices.md)

**Related topics**  


[Map multiple application services suggested by classic Service Mapping](map-business-services-in-bulk.md)

[Map application services using tags with classic Service Mapping](map-service-tag.md)

[Map multiple application services from a CSV file using classic Service Mapping](import-business-services-csv.md)

[Fix application service errors in bulk](fix-bus-serv-errors-by-category.md)

[Fix errors in individual application service maps](fix-or-ignore-errors-business-service-map.md)

[Review and approval of application service maps](business-service-approval.md)

[Fine-tune application services to implement owner requests](review-implement-business-service-maps.md)

[Application service completion](../concept/advanced-business-service-definitions.md)

[Application service analysis and maintenance using classic Service Mapping](../concept/c_SvcPlanningAndAnalysisUsingMaps.md)

