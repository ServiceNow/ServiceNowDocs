---
title: Exclude preconfigured CI relationships in tag-based discovery
description: Exclude preconfigured CI relationships from the tag-based discovery process to refine the application services created. Service Mapping consists of preconfigured CI relationships and includes CIs in these relationships even if they do not have assigned tags. Choose which preconfigured CI relationships to exclude and the remaining CI relationships participate in tag-based discovery.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Tag-based discovery configuration, Advanced Service Mapping configuration, Configuring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Exclude preconfigured CI relationships in tag-based discovery

Exclude preconfigured CI relationships from the tag-based discovery process to refine the application services created. Service Mapping consists of preconfigured CI relationships and includes CIs in these relationships even if they do not have assigned tags. Choose which preconfigured CI relationships to exclude and the remaining CI relationships participate in tag-based discovery.

## Before you begin

Learn about default feature configuration in [Tag-based discovery in Service Mapping](../concept/tag-based-mapping.md).

**Note:** Starting with Service Mapping Plus version 1.16.3, take advantage of the Tag-based Service Mapping workspace to efficiently map you application services. For more information, see [Tag-based mapping in the Service Mapping Workspace](../reference/tag-based-mapping-dashboard.md) and [Tag-based discovery for the Service Mapping Workspace](../concept/tag-discovery-service-mapping-workspace.md).

Role required: service\_mapping\_admin

## About this task

The Traversal Rules for Application Services \[svc\_traversal\_rules\] table stores the CI relationships that participate in tag-based discovery. By default, preconfigured CI relationships used in tag-based discovery have the **true** value in the **Base System Rule** column. Use this information to exclude preconfigured CI relationships from tag-based discovery.

**Important:** You cannot delete or modify preconfigured CI relationships used for tag-based discovery from the Traversal Rules for Application Services \[svc\_traversal\_rules\] table.

## Procedure

1.  Navigate to **Service Mapping** &gt; **Administration** &gt; **Tag-based Service Traversal Rules**.

    ![Table containing information on CI relationships used in tag-based discovery.](../image/traversal-rules-application-services-table.png)

2.  Click the preconfigured CI relationship you want to exclude from tag-based discovery.

    To view these CI relationships, see [Preconfigured CI relationships in tag-based discovery](../reference/ci_relationships_tag_mapping.md)

3.  Clear the **Active** check box.

4.  Click **Submit** in the **Traversal Rules for Application Services** form.


## What to do next

If you refine the default configuration after creating appliations based on tags, see [Recalculate previously created application services](recalculate_application_services.md) for the next steps.

**Parent Topic:**[Tag-based discovery configuration](../concept/tag_discovery_configuration.md)

