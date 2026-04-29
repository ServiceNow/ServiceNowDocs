---
title: Include CIs based on classes in tag-based discovery
description: Use CI classes to identify which CIs Service Mapping includes in application services during tag-based discovery. By default, this list appears empty and includes all CIs belonging to all CI classes. Define CI classes and allow only CIs belonging to these classes or their extensions to participate in tag-based discovery.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Tag-based discovery configuration, Advanced Service Mapping configuration, Configuring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Include CIs based on classes in tag-based discovery

Use CI classes to identify which CIs Service Mapping includes in application services during tag-based discovery. By default, this list appears empty and includes all CIs belonging to all CI classes. Define CI classes and allow only CIs belonging to these classes or their extensions to participate in tag-based discovery.

## Before you begin

Learn about default feature configuration in [Tag-based discovery in Service Mapping](../concept/tag-based-mapping.md).

**Note:** Starting with Service Mapping Plus version 1.16.3, take advantage of the Tag-based Service Mapping workspace to efficiently map you application services. For more information, see [Tag-based mapping in the Service Mapping Workspace](../reference/tag-based-mapping-dashboard.md) and [Tag-based discovery for the Service Mapping Workspace](../concept/tag-discovery-service-mapping-workspace.md).

Role required: service\_mapping\_admin

## Procedure

1.  Navigate to **Service Mapping** &gt; **Administration** &gt; **Properties**.

2.  Enter CI classes, separated by commas, in the allow list that controls which tagged CIs participate in tag-based mapping.

    ![Allow list used to define CI classes and control which CIs participate in tag-based mapping](../image/service-mapping-properties-allow-list.png)

3.  Click **Save**.


## What to do next

If you refine the default configuration after creating appliations based on tags, see [Recalculate previously created application services](recalculate_application_services.md) for the next steps.

**Parent Topic:**[Tag-based discovery configuration](../concept/tag_discovery_configuration.md)

