---
title: Tag-based discovery for the Service Mapping Workspace
description: If your organization uses tags for asset management, you can use the Service Mapping workspace to manage these tags and create tag-based application services.
locale: en-US
release: zurich
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Choose method for discovering and mapping services, Exploring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Tag-based discovery for the Service Mapping Workspace

If your organization uses tags for asset management, you can use the Service Mapping workspace to manage these tags and create tag-based application services.

A tag is a label that consists of a key-value pair, used to categorize and organize assets within your organization. Tags enhance query and reporting capabilities, making it easier to manage and track resources. Unlike other mapping methods, tag-based mapping does not require configuring credentials or providing users with elevated rights. You can effectively use tags to map multiple service instances. Discovery and Cloud Provisioning and Governance can automatically detect tags from all major cloud providers and container ecosystems. Once these tags are discovered, Service Mapping can leverage them to create and manage application services. This approach is useful for resource management in virtualized, hyper-converged, and multi-cloud environments.

For information about the traditional tag-based discovery process, see [Tag-based discovery in Service Mapping](tag-based-mapping.md). Tag-based discovery for the Service Mapping workspace operates differently and consists of the following stages:

**Note:**

Access to tag-based service mapping in the Service Mapping workspace requires the installation of Service Mapping Plus version 1.16.3.

1.  Discovery and Cloud Provisioning and Governance discover tags for cloud and resource configuration items \(CIs\) and then populate data for discovered tags into the Key Value \[cmdb\_key\_value\] table.
2.  The administrator creates CI tag categories and defines tag keys that the categories contain. Tag categories contain tags with similar use. For example, if your organization has production and staging environments, you could create "production" and "staging" tag values.

    **Note:** Starting with version 1.7.0, Tag Governance offers five predefined categories that you can use without modification. Administrators can also modify these categories or add new ones.

3.  The process begins with the selection of a tag category from the available categories or a category that the administrator creates.
    -   Only CIs with discovered tag keys for the selected tag categories become part of application services.
    -   The administrator can narrow the criteria by defining specific tag values in addition to tag categories.
    -   Service Mapping uses only CIs that have the matching values to create application services with the service family being created automatically.
4.  Service Mapping queries the CMDB for CIs with tag values that match the tag definitions for the selected categories.
5.  Service Mapping creates service candidates based on the defined tags.
6.  The administrator selects the service candidates to map, starts the mapping process, and names the tag-based service family. This record is saved so the administrator can return at any time to monitor or continue the process later.
7.  Service Mapping adds new application services to the Tag-Based Application Service \[cmdb\_ci\_service\_by\_tags\] table.

    **Important:** Service instances mapped using tags might not include relevant CIs if those CIs do not have the correct tags.

8.  The tag-based service content is calculated on demand either when the map is first viewed or initiated manually.

    Service Mapping maps application services by creating connections between tagged CIs based on CI relationships. The Traversal Rules for Application Services \[svc\_traversal\_rules\] table contains information used for creating tag-based application services.

    The Manual CI Exclusions/Inclusions \[svc\_manual\_ci\_exclusions\_inclusions\] table can filter out CI classes, helping to prevent them from being added by tags or traversal rules.

    **Note:** Service Mapping includes CIs that are part of these relationships even if these CIs do not have tags assigned to them.


**Related topics**  


[Tag-based mapping in the Service Mapping Workspace](../reference/tag-based-mapping-dashboard.md)

[Map your application services using tags in the Service Mapping Workspace](../task/map-tag-based-services-workspace.md)

