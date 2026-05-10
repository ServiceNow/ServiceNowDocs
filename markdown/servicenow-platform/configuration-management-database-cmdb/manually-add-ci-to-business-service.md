---
title: Manually add CIs to an application service
description: Add configuration items to manually created application services or to services discovered by Service Mapping.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Service instances \(Application services\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Manually add CIs to an application service

Add configuration items to manually created application services or to services discovered by Service Mapping.

## Before you begin

-   Verify that the CI type for the configuration item \(CI\) that you are planning to add, exists. If necessary, create the CI type as described in [Create CI types for Service Mapping and Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/t_CreateCITypeForSM.md).
-   Add CIs to the CMDB for the device or application that you want to add, if necessary. See [Populate the CMDB](../../configuration-management/concept/c_OptionsToPopulateCMDB.md) for more information.

Role required: app\_service\_admin or service\_mapping\_admin

## About this task

Adding a CI to an application service requires creating a relationship between the new CI and a CI in the application service. You can add CIs to an application service that was created manually, by either:

-   Adding a method to populate the application service.

    Navigate to **CSDM** &gt; **Manage Technology Management Services** &gt; **Application Service**. Select an application service and then use the **Populate the Application Service** tab to choose a method to populate the application service. For more details, see [Create an application service](create-it-services.md).

-   Using the application service service map as described in the steps below.

    The default relationship type of the added connection in this case is **Depends on::Used by**. You can modify this default relationship type by changing the value of the **sa.it\_service.manual\_ci\_rel\_type** property. See [Components installed with application services](../../configuration-management/reference/components-installed-app-services.md) for more information.


**Important:** You cannot fine-tune or edit tag-based and dynamic services from the map.

Manually adding a new CI to an existing CI in a service instance prompts the CMDB to update the information about both CIs, including their relationship type. If other application services use the same applicative flow, the CMDB recognizes the new CI and automatically adds it to those services as well.

For example, you manually add an IBM WebSphere Message Broker to an IBM WebSphere HTTP Listener in the Bank Customer Portal service. The system also adds this IBM WebSphere Message Broker to the same HTTP Listener in the Bank Internal Portal service, because it uses this HTTP Listener. Similarly, when you remove a CI you added manually, the system removes it from all application services where you either manually added it or it was automatically added by analogy.

You can manually connect a CI only to actual CIs existing in the CMDB, not to a visualization of other items on the map such as clusters or boundaries. Also, you cannot add CIs of these CI types to an application service:

-   NAT \[cmdb\_ci\_translation\_rule\]
-   Endpoint \[cmdb\_ci\_endpoint\]
-   Qualifier \[cmdb\_ci\_qualifier\]
-   Application cluster \[cmdb\_ci\_application\_cluster\]

There are system records in the Manual CI Exclusions/Inclusions \[svc\_manual\_ci\_exclusions\_inclusions\] table. See [Components installed with application services](../../configuration-management/reference/components-installed-app-services.md#manual-ci-inclusion-exclusion-list) for more information.

**Note:** The Manual CI Exclusions/Inclusions \[svc\_manual\_ci\_exclusions\_inclusions\] table doesn't include CIs added using traversal rules.

In environments with domain separation, only CIs belonging to the same domain as the service instance are added to the service instance. If there is a domain hierarchy, CIs must belong to the same child domain as the service instance.

If working with an service instance discovered by Service Mapping, manually add a CI:

-   To indicate that an service instance contains a device or application, which Service Mapping cannot discover. For example, add an A/C unit to the Production Floor service.
-   To add a temporary placeholder for a CI, which Service Mapping did not discover. In this case you are planning to perform necessary troubleshooting to ensure that Service Mapping discovers this CI in the future. For example, add an IBM WebSphere Message Broker to the Bank Customer Portal service.
-   To create an service instance that combines entry points and CIs automatically discovered by Service Mapping with entry points and CIs from the CMDB. After you manually add an entry point, you can update the service instance with CIs from the CMDB based on the relationships defined there.

For additional information related to Service Mapping, see [Pattern customization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/c_MappingPatternsCustomization.md) and [Enable traffic-based discovery for CI types or specific CIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/t_CreateATrafficBasedDiscoveryRule.md).

## Procedure

1.  Open the service instance map.

    1.  Navigate to **All** &gt; **CSDM** &gt; **Manage Technology Management Services** &gt; **Service Instance**.

    2.  Select the needed service instance.

    3.  On the service instance page, select **View Map**.

2.  If needed, click **Edit** to ensure that the map is in Edit mode.

    If Service Mapping is deployed, then in Edit mode, the Discovery Messages section appears below the map.

3.  To connect a CI to another CI on the map, right-click the CI to which you want to connect the new CI, and then select **Add a CI**.

4.  In the Add A CI dialog box, specify the CI to add:

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
</table>    The CI type list includes only allowed CI types. For example, you cannot add an application cluster.

5.  Click **Submit**.

    The manually added CI appears on the map.

    **Note:** When you manually add a CI, which is an application, as a child to a service that already includes its parent application CI, the newly added child application CI is hidden inside the inclusion. Click the plus \(+\) symbol next to the parent application CI to see the child application CI.

6.  If Service Mapping is activated, add a discoverable outgoing connection for the manually added CI:

    1.  Right-click the manually added CI.

    2.  Select **Manually add a connection**.

        **Note:** If you do not see the **Manually add a connection** option in the right-click menu, check that you are logged in with the user that belongs to the same domain as the application service.

    3.  Configure attributes for the entry point as described in [Entry points attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/r_EntryPointsforBizSvcDef.md).

    4.  Click **Submit**.

        Discovery and Service Mapping attempt to discover this CI. If successful, the CI appears on the map. Otherwise, a warning icon \(![The Warning icon](../image/MapWarningIcon.png)\) appears.

7.  If Service Mapping is activated and you want Service Mapping to automatically discover a CI, which you previously added manually:

    1.  Customize the relevant pattern or fine-tune traffic-based discovery to enable Service Mapping to discover the CI.

    2.  Navigate to the relevant service instance map.

    3.  Click **Run discovery**.

    4.  After the discovery process finishes, verify that Service Mapping discovered the CI by checking the connector leading to the CI.

        If Service Mapping discovered the CI, then two connectors, a manual and automatically discovered, appear for the CI.

        ![Manually added CI, which Service Mapping later discovered automatically.](../image/MapManualCIRediscoveredCI.png)

    5.  Right-click the CI you added manually.

        In the example, it is IBM WebSphere Message Broker.

    6.  Select **Remove manually added CI**.

        The map shows the CI with only one connector leading to it. If this CI had any manually added connections, they are removed together with the manually added CI.


**Related topics**  


[Link application services](link-services-to-services.md)

[addCI\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/BusinessServiceManagerAPI.md)

