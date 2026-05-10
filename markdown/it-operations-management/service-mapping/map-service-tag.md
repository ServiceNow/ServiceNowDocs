---
title: Map application services using tags with classic Service Mapping
description: Use tags that help categorize and organize configuration items \(CIs\) in your organization to map application services. Tag-based mapping doesn't require configuring credentials or providing users with elevated rights.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Map application services using tags with classic Service Mapping

Use tags that help categorize and organize configuration items \(CIs\) in your organization to map application services. Tag-based mapping doesn't require configuring credentials or providing users with elevated rights.

## Before you begin

Analyse, review, and define tags as covered in [Prepare for mapping application services based on tags](prepare-map-service-tag.md).

Role required: service\_mapping\_admin

## About this task

A tag is a label that consists of a key-value pair. Your organization may use tags to categorize its assets, to enhance query and reporting capabilities. Discovery and Cloud Provisioning and Governance can discover tags used by all major cloud providers and container ecosystems. Once the tags are discovered, Service Mapping can create service instances based on these tags. For example, you can use tags to map all application services your organization uses in the production environment in the EMEA region. You can effectively use tags to map multiple service instances.

**Note:** Starting with Service Mapping Plus version 1.16.3, take advantage of the Tag-based Service Mapping workspace to efficiently map you application services. For more information, see [Tag-based mapping in the Service Mapping Workspace](../reference/tag-based-mapping-dashboard.md) and [Tag-based discovery for the Service Mapping Workspace](../concept/tag-discovery-service-mapping-workspace.md).

The result of the tag-based mapping is a hierarchical service map that may be less precise than the application service created using the patterns.

![Comparison of pattern-based and tag-based mapping results](../image/pattern-vs-tags-maps-comparison.png "Comparison of pattern-based and tag-based mapping results")

Service Mapping creates names for tag-based services using tag values discovered for the tag definitions, to which these tag-based services belong. For example, for Environment and Application tag categories with Production and HR as their respective tag values, the default service name is production::hr. Tag-based service names use low case.

**Important:** If you add or remove tag categories after mapping services, Service Mapping does not implement these changes for previously mapped services belonging to this service family. For more information, see [Modify or update tag definitions for tag-based mapping](modify-tag-category-family.md).

In domain-separated deployments, Service Mapping populates tag-based services based on this service family only with CIs belonging to the leaf domain to which the service family belongs.

To map a single application service using tags without preliminary configuration, use the flow based on Common Service Data Model. For more information, see [Populate application services using tags](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/populate-app-service-tags.md).

**Note:** Starting with version 1.15.2, there is a limit of 200 application service candidates per family.

## Procedure

1.  Navigate to **Service Mapping** &gt; **Administration** &gt; **Tag-based Service Families**.

2.  Click **New**.

3.  Define the service family name.

4.  Select **Regularly update service candidates** for Service Mapping to regenerate suggestions for service instances that match tag categories you define for the service family.

5.  Define the tag categories and tag values to use for mapping service instances belonging to this service family.

    1.  Under **Selected tag categories**, select the relevant tag category from the list of tag categories you defined earlier.

    2.  To make the mapping process more precise, add the tag value, for example, Production.

        For multiple tag values, use comma as a separator: Staging, Production.

    3.  To change the default service naming convention, set the order in which Service Mapping uses the tag values in the candidate name.

        For example, the first category of the service family is Environment and the second category is Application. The default service name that Service Mapping assigns to the service candidate is Production::Finance. To make Service Mapping use the Application category value at the beginning of the name, set the Order value for the Application category to 1.

    4.  Select other tag categories as necessary for this service family.

        The maximum number of categories per service family is three.

6.  Click **View service candidates.**

7.  In the Service candidate window, review the suggested service candidates and select the ones that you want to map.

    If there are no service candidates, in the Key Value \[cmdb\_key\_value\] table, ensure that there are tag values for the tag keys you used for mapping.

8.  Click **Map selected**.

    Service Mapping creates service instances based on the candidates you selected.

    If there is an error about the service name that exists in the system, fix the candidate name by performing the following steps:

    1.  Click **View service candidates**.

    2.  Click the name that exists and change it.

    3.  Click **OK** ![OK button](../image/BusinessMappingOKicon.png) to save the change.

    4.  View the service candidates and map the relevant ones.

        New candidates contain only the service instance CIs as their entry points. The Populate Calculated Services scheduled job maps new tag-based services once a day.

9.  To map a new service instance immediately, without waiting for the scheduled job to populate it:

    1.  Select the relevant service instance.

    2.  In the service instance form, click **Additional Info** on the left.

    3.  Under **Related Links**, click **Recalculate Service**.

    4.  Click **View Map** at the top of the form and review the mapping result.

10. After the scheduled job maps all new tag-based services, navigate to the relevant tag-based service family and review the newly mapped services listed under **Mapped services**.


## Result

All tag-based service instances have their respective service instance CIs as their entry points.

![Tag-based service map.](../image/tag-based-map-example.png "The map for the Finance::Production service instance based on tags")

## What to do next

1.  After the scheduled job maps all new tag-based services, navigate to the relevant tag-based service family and review the newly mapped services listed under **Mapped services**.
2.  Make sure that the service instances aren't too large: The following discovery message is displayed in a tag-based service instance: **This tag-based service instance reached the maximum number of CIs. For more information, refer to the product documentation.**

    If some application services are too large, resolve the service size issue:

    -   [Modify tag definitions used for mapping](modify-tag-category-family.md) to make sure Service Mapping includes only relevant CIs in the service instance.
    -   If necessary, [Tag-based discovery configuration](../concept/tag_discovery_configuration.md) to change which CIs Service Mapping includes in tag-based service instances.
3.  To fine-tune or fix the tag-based services, [modify the tag categories](modify-tag-category-family.md) that you used for the service family.

    **Important:** The map window displays maps for tag-based and dynamic services in the View mode only. You cannot fine-tune or edit tag-based and dynamic services from the map.


-   **[Prepare for mapping application services based on tags](prepare-map-service-tag.md)**  
Analyze, review, and define tags in your organization for successful mapping.

**Parent Topic:**[Application service mapping using classic Service Mapping](../concept/c_DefineMapBusinessServices.md)

**Related topics**  


[Map multiple application services suggested by classic Service Mapping](map-business-services-in-bulk.md)

[Map multiple application services from a CSV file using classic Service Mapping](import-business-services-csv.md)

[Map a single application service using classic Service Mapping](t_DefineNewBusinessService.md)

[Fix application service errors in bulk](fix-bus-serv-errors-by-category.md)

[Fix errors in individual application service maps](fix-or-ignore-errors-business-service-map.md)

[Review and approval of application service maps](business-service-approval.md)

[Fine-tune application services to implement owner requests](review-implement-business-service-maps.md)

[Application service completion](../concept/advanced-business-service-definitions.md)

[Application service analysis and maintenance using classic Service Mapping](../concept/c_SvcPlanningAndAnalysisUsingMaps.md)

[Choose the right method for discovery and mapping application services](../concept/choose-mapping-method.md)

[Tag-based discovery configuration](../concept/tag_discovery_configuration.md)

