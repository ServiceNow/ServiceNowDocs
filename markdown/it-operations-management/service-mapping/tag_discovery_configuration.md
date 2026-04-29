---
title: Tag-based discovery configuration
description: You can refine the default configuration to control which CIs Service Mapping includes in application services during the tag-based discovery process.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Advanced Service Mapping configuration, Configuring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Tag-based discovery configuration

You can refine the default configuration to control which CIs Service Mapping includes in application services during the tag-based discovery process.

**Note:** Starting with Service Mapping Plus version 1.16.3, take advantage of the Tag-based Service Mapping workspace to efficiently map you application services. For more information, see [Tag-based mapping in the Service Mapping Workspace](../reference/tag-based-mapping-dashboard.md) and [Tag-based discovery for the Service Mapping Workspace](tag-discovery-service-mapping-workspace.md).

Service Mapping provides preconfigured CI relationships which can participate in tag-based discovery. You have the ability to customize these CI relationships and refine the default configuration using one of the following methods:

-   include CIs based on classes in tag-based discovery;
-   exclude CIs based on their install status;
-   exclude preconfigured CI relationships;
-   add or edit CI relationships.

To view preconfigured CI relationships which Service Mapping includes in application services during tag-based discovery, see [Preconfigured CI relationships in tag-based discovery](../reference/ci_relationships_tag_mapping.md).

To view properties installed with Service Mapping that relate to tag-based discovery, see [Properties related to tag-based discovery](../reference/properties_tag_mapping.md).

-   **[Include CIs based on classes in tag-based discovery](../task/include_cis_tag_discovery_configuration.md)**  
Use CI classes to identify which CIs Service Mapping includes in application services during tag-based discovery. By default, this list appears empty and includes all CIs belonging to all CI classes. Define CI classes and allow only CIs belonging to these classes or their extensions to participate in tag-based discovery.
-   **[Exclude CIs based on their installation status in tag-based discovery](../task/exclude_cis_install_status_tag_mapping.md)**  
Use the CI installation status to create CI classes and exclude CIs from application services during tag-based discovery. By default, application services based on tags exclude CIs with the Retired or Absent install status. You can expand this list of excluded CIs to include additional installation statuses such as Pending install or Stolen.
-   **[Exclude preconfigured CI relationships in tag-based discovery](../task/exclude_ci_relationships_tag_mapping.md)**  
Exclude preconfigured CI relationships from the tag-based discovery process to refine the application services created. Service Mapping consists of preconfigured CI relationships and includes CIs in these relationships even if they do not have assigned tags. Choose which preconfigured CI relationships to exclude and the remaining CI relationships participate in tag-based discovery.
-   **[Add or edit CI relationships in tag-based discovery](../task/edit_ci_relationships_tag_mapping.md)**  
Activate pre-configured CI relationships that Service Mapping does not include by default or add additional relationships to use in the tag-based discovery process. For example, you can add a CI relationship between Linux servers and storage devices to discover servers hosting storage devices based on tags.
-   **[Recalculate previously created application services](../task/recalculate_application_services.md)**  
Recalculate application services after you refine the default configuration to control which CIs to include during the tag-based discovery process.

**Parent Topic:**[Advanced Service Mapping configuration](c_ConfigureSM.md)

