---
title: Remap tag-based application services to reflect tag changes
description: Recreate tag-based services if the way your organization uses tags have changed or after modifying tag definitions for tag-based service families.
locale: en-US
release: zurich
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Modify or update tag definitions for tag-based mapping, Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Remap tag-based application services to reflect tag changes

Recreate tag-based services if the way your organization uses tags have changed or after modifying tag definitions for tag-based service families.

## Before you begin

If necessary, modify the tag definitions for the relevant tag-based service family.

Role required: service\_mapping\_admin

## About this task

Remap existing tag-based services after you have manually modified tag definitions. If your organization uses new tag keys or tag values, you may also want to remap existing services. In both cases, Service Mapping does not automatically update existing services to reflect tag changes.

## Procedure

1.  Navigate to **Service Mapping** &gt; **Administration** &gt; **Tag-based Service Families**.

2.  Select the tag-based service family for which tag definitions have changed.

3.  Under **Related Links**, click **Manually update candidates** to generate new service candidates using the modified tag definitions.

4.  In the Service candidate window, review the suggested service candidates and select the ones that you want to map.

    If there are no service candidates, ensure that you selected the tag values that exist in the Key Value \[cmdb\_key\_value\] table.

5.  Click **Map selected**.

    Service Mapping creates application services based on the candidates you selected.

6.  Under **Mapped services**, review the newly created services to ensure that the result is as you expected.

    If Service Mapping offers to view the CI list instead of a map for an application service, this service is too large. Fine-tune it as described in [modify the tag categories](modify-tag-category-family.md).


## Result

You have mapped the application service based on the latest tag definitions.

![Remapped tab-based application service.](../image/remap-tag-based-map-example.png "Remapped tab-based application service")

## What to do next

Make sure that the service instances aren't too large:

-   Service Mapping doesn't offer to view CI list instead of a map for a service instance.
-   There is no discovery message indicating that the service instance is too large: **The map does not display the entire service, because it is too large. The number of CI connections exceeded the allowed maximum.**

If the service is too large, perform the following actions:

-   [Modify tag definitions used for mapping](modify-tag-category-family.md) to make sure Service Mapping includes only relevant CIs in the service instance.
-   If necessary, [Tag-based discovery configuration](../concept/tag_discovery_configuration.md) to change which CIs Service Mapping includes in tag-based service instances.

**Parent Topic:**[Application service mapping using classic Service Mapping](../concept/c_DefineMapBusinessServices.md)

