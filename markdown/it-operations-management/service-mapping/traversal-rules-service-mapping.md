---
title: Traversal rules in Service Mapping
description: Traversal rules identify and map relationships between configuration items to create comprehensive application service maps. They connect relevant configuration items based on predefined relationships, promoting accurate service mapping and visualization.
locale: en-US
release: xanadu
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2025-11-04"
reading_time_minutes: 2
breadcrumb: [Exploring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Traversal rules in Service Mapping

Traversal rules identify and map relationships between configuration items to create comprehensive application service maps. They connect relevant configuration items based on predefined relationships, promoting accurate service mapping and visualization.

Traversal rules facilitate comprehensive service mapping by identifying related configuration items \(CIs\) through specific relationships that exist in the Configuration Management Database \(CMDB\). These rules support the mapping of related CIs even when they aren’t directly tagged, providing a more accurate service map.

## Components of traversal rules

When configuring traversal rules, it’s essential to add them in the correct order, as tag-based discovery uses these rules to identify CIs that can be mapped.

The Service Mapping administrator \(service\_mapping\_admin\) manages traversal rules in the Traversal Rules for Application Services \[svc\_traversal\_rules\] table. When configuring these rules, the following key components are considered:

-   **Parent Type:** The CI class that serves as the starting point for mapping related configuration items that belong to the Child class as specified by the traversal rule.
-   **Relationship:** The specific association or link between the Parent CI and Child CI that determines how they’re related in the service mapping context. The direction of the traversal depends on the **Is Reverse** setting.
-   **Child Type:** The CI class that contains the related configuration items being mapped from the Parent CI class as specified by the traversal rule.
-   **Priority Level:** The level that specifies the order in which traversal rules are applied, with lower numbers taking precedence over higher numbers.
-   **Is Reverse:** A flag that determines the direction of traversal for the relationship between Parent CI and Child CI. When selected, the mapping process starts from the Child CI instead of the Parent CI.

    **Note:** To promote accurate mapping, configure traversal rules with the correct priority levels, as tag-based discovery relies on these rules to identify mappable CIs.


## Configuring traversal rules

Service Mapping includes predefined traversal rules, simplifying the initial configuration. These rules provide a starting point for your tag-based service mapping setup. For details on the specific predefined rules, see [Predefined traversal rules for application services in Service Mapping](../reference/default-traversal-rules.md).

In addition to these predefined traversal rules, you can configure custom traversal rules to meet your organization's specific needs. For detailed instructions on how to configure traversal rules, including information on the required fields and settings, see [Traversal Rules for Application Services form completion](../reference/traversal_rules_form_completion.md).

By default, you can only have five traversal rules participate in tag-based discovery. However, you can adjust this limit by configuring the **sys\_property svc\_traversal.rules.active** system property to enable more active traversal rules.

**Parent Topic:**[Exploring Service Mapping](service-mapping-get-started.md)

