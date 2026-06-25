---
title: Modify or update tag definitions for tag-based mapping
description: You can change tag definitions that Service Mapping uses for tag-based mapping. Service Mapping uses updated tag definitions to create new tag-based services without applying tag-related changes to services you mapped earlier.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/service-mapping/modify-tag-category-family.html
release: australia
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Modify or update tag definitions for tag-based mapping

You can change tag definitions that Service Mapping uses for tag-based mapping. Service Mapping uses updated tag definitions to create new tag-based services without applying tag-related changes to services you mapped earlier.

## Before you begin

If you need to create a new tag category or modify an existing tag category, follow the prerequisites in [Map application services using tags with classic Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/map-service-tag.md).

Review recommendations in [Prepare for mapping application services based on tags](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/prepare-map-service-tag.md).

Role required: service\_mapping\_admin

## About this task

**Note:** Starting with Service Mapping Plus version 1.16.3, take advantage of the Tag-based Service Mapping workspace to efficiently map you application services. For more information, see [Tag-based mapping in the Service Mapping Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/tag-based-mapping-dashboard.md) and [Tag-based discovery for the Service Mapping Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/tag-discovery-service-mapping-workspace.md).

You may decide to add or remove tag categories from a tag-based service family in the following cases:

-   If you are not satisfied with the results of the tag-based mapping, for example, if the service is too large, because it includes irrelevant CIs.
-   If there are changes in the way your organization uses tags, for example there are new tags.

When you modify tag categories defined for a tag-based service family or delete a tag-based family itself, the system detaches all mapped services from this tag-based service family. These services still exist and Service Mapping continues to update them using the original tag definition. To avoid having tag-based services based on outdated tag definitions, delete existing tag-based services.

Service Mapping generates new tag-based service candidates that you use to map services based on modified tag definition.

**Important:** New services based on modified tag definitions do not overwrite previously mapped services.

## Procedure

1.  Delete existing tag-based services:

    1.  Navigate to **Service Mapping** &gt; **Administration** &gt; **Tag-based Service Families**.

    2.  Select the tag-based service family for which you want to modify the tag definition.

    3.  Under **Mapped services**, click **Delete mapped services** to delete all services.

    4.  Alternatively, click the **Mark for deletion** icon next to the relevant service in the list, and then click **Delete**.

2.  Navigate to **Service Mapping** &gt; **Administration** &gt; **Tag-based Service Families**.

3.  Select the tag-based service for which you want to modify the tag definition.

4.  Under **Selected tag categories**, perform one of the following actions:

    -   Add a new tag category by double-clicking the empty row and selecting the relevant tag category from the list of tag categories you defined earlier.
    -   Remove a tag category by clicking the **Mark for deletion** icon next to it.
    -   Modify the use of a tag category already associated with the service family by changing the tag values or the service naming order.

        For multiple tag values, use comma as a separator. The service naming order defines how Service Mapping uses the tag category name in the names of application services generated for the service family.

    -   Modify the tag category itself by clicking the tag category name and then defining the CI tag keys.
5.  Click **Update**.


## What to do next

[Remap tag-based application services to reflect tag changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/remap-tag-based-services-tag-changes.md)

**Parent Topic:**[Application service mapping using classic Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/c_DefineMapBusinessServices.md)

**Related topics**  


[Map multiple application services suggested by classic Service Mapping]()

[Map application services using tags with classic Service Mapping]()

[Map multiple application services from a CSV file using classic Service Mapping]()

[Map a single application service using classic Service Mapping]()

[Fix application service errors in bulk]()

[Fix errors in individual application service maps]()

[Review and approval of application service maps]()

[Fine-tune application services to implement owner requests]()

[Application service completion]()

[Application service analysis and maintenance using classic Service Mapping]()

