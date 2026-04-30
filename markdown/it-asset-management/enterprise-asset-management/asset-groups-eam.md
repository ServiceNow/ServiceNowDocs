---
title: Asset groups in Enterprise Asset Management
description: Asset groups in Enterprise Asset Management provide organizations with a systematic approach to asset structuring for complex asset ecosystems thereby improving data integrity and providing actionable insights.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Explore, Enterprise Asset Management, IT Asset Management]
---

# Asset groups in Enterprise Asset Management

Asset groups in Enterprise Asset Management provide organizations with a systematic approach to asset structuring for complex asset ecosystems thereby improving data integrity and providing actionable insights.

## Overview of asset groups in Enterprise Asset Management

An asset group is a logical grouping of assets.

Asset groups can be used in the Enterprise Asset Workspace, Facility Asset Workspace, Medical Asset Workspace, and the Operational Technology \(OT\) Asset Workspace.

An asset group can have multiple subgroups; however a subgroup can be a part of only one asset group. Asset groups and subgroups can have assets and an asset can belong to multiple groups.

Asset groups are listed in the Asset groups subtab, located within the Asset groups tab in the Enterprise asset estate view. The asset groups and the descendant asset groups are displayed in a content tree. For details on creating asset groups and subgroups, see [Create an asset group in Enterprise Asset Management](../task/create-asset-groups-eam.md) and [Create an asset subgroup in Enterprise Asset Management](../task/create-asset-subgroup-eam.md).

Enterprise Asset Management administrators can configure the **Asset groups** tab to show or hide in the Enterprise Asset Workspace, Facility Asset Workspace, Medical Asset Workspace, and the OT Asset Workspace. For more details, see [Configure tabs in the Enterprise Asset Workspace](../task/configure-model-asset-class-tabs.md).

An asset group or subgroup can optionally refer to a service instance that helps in pulling in all related assets from a chosen node in that hierarchy. Alternatively, a subgroup can be defined without referencing the subgroup to a service instance, allowing users to manually select assets. For details on adding assets to asset groups, see [Add assets to an asset group or subgroup](../task/add-assets-assetgroups.md).

A subgroup inherits some fields from its parent group. For details on the fields that get inherited, see [Fields inherited from a parent asset group to a sub group](../reference/subgroups-parent-fields-eam.md).

## Sites in asset groups

A site is an ISA-95 hierarchical entity model. Sites are entity records in the Equipment Model Entity \[cmdb\_ci\_ot\_isa\_entity\] table, organized in a hierarchical structure with site being the top-level entity, followed by area, work center, and work unit. Each level of the ISA-95 entity model can be associated with CIs.

You can associate an asset group to a site. Associating an asset group to a site enables all CIs associated with that specific site to be also associated with the asset group.

**Note:** Only assets from the associated site and its specific location can be added to the asset group. You don’t have access to add assets from outside the associated site and location.

If an asset group references a service instance, and that service instance is an entity record in the Equipment Model Entity \[cmdb\_ci\_ot\_isa\_entity\] table, the **Site** field in the asset group record is automatically populated.

If an asset group doesn't refer to a service instance, or it's referring to a service instance that doesn't have entity records in the cmdb\_ci\_ot\_isa\_entity​ table, then a site for that asset group doesn't exist and that asset group gets listed under the Unassigned site group in the Asset groups subtab.

All sites for asset groups are listed in the Sites subtab, located within the Asset groups tab in the Enterprise asset estate view. For details on creating sites, see [Create sites in the Enterprise Asset Management](../task/create-sites-eam.md).

## Considerations for asset groups

The following are some considerations to keep in mind for asset groups:

-   An asset group can’t contain itself as a sub group.
-   An asset group can’t have a model or model category as it's a separate entity.
-   An asset group can have a service instance link only if its parent group has one or if it has no parent.
-   An asset group can't be deleted if it contains subgroups and assets. To delete an asset group, the sn\_eam.enterprise\_asset\_manager or the sn\_eam.enterprise\_admin role must first remove the subgroups and assets within the asset group.

## Considerations for adding assets to asset groups

The sn\_eam.enterprise\_admin role and the sn\_eam.enterprise\_asset\_manager role can create asset groups and add assets to asset groups.

The **Service instance** field on the asset form refers to the Application Service \[cmdb\_ci\_service\_auto\] table and to its following descendant tables:

-   Mapped Application Service \[cmdb\_ci\_service\_discovered\] table
-   Calculated Application Service \[cmdb\_ci\_service\_calculated\] table
-   Equipment Model Entity \[cmdb\_ci\_ot\_isa\_entity\] table

Keep the following considerations in mind while adding assets to asset groups:

-   If the asset group isn’t referring to a service instance, the cmdb\_ci\_service\_auto table, or any of its descendent tables, you can add any asset that is not included in any asset group.
-   If the asset group is referring to a service instance, the cmdb\_ci\_service\_auto table, or any of its descendent tables, you can add assets whose asset CI has a CI relationship to the service instance, the cmdb\_ci\_service\_auto table, or any of its descendent tables, referenced by the asset group.​
-   You can only add assets without a parent.​ The child assets won’t be added automatically to the asset group. Any assets that have as their parent the asset that was just added to the asset group won’t be added automatically. For example, you add a pre-assembled asset that has no parent. The child assets of that pre-assembled asset won’t also be added.
-   Assets that are from the same location as the asset group’s location or a descendent of the asset group’s location.
-   Only hardware and enterprise assets can be added.
-   Consumable asset, linear assets, linear segments, and pallets can't be added.​
-   If a subgroup isn’t referring to a service instance, the cmdb\_ci\_service\_auto table, or any of its descendent tables, but an ancestor asset group is referring to a service instance, the cmdb\_ci\_service\_auto table, or any of its descendent tables, you can only add assets whose asset CI has a CI relationship to a service instance, the cmdb\_ci\_service\_auto table, referenced by the ancestor asset group. ​
-   Asset should only be in the **In use** or **In maintenance** state.​​

## Considerations for asset groups in flows and in the Enterprise Asset Workspace

Asset groups won't be available in the following flows and scenarios:

-   Asset resale flow.
-   Transfer order lines.
-   Repair order lines.
-   Disposal orders.
-   While creating shipment assets.
-   Contracts.
-   Move orders.
-   Any flow where the asset requires a model.

Additionally, the asset hierarchy contextual side panel doesn't appear for asset groups and all assets and enterprise assets lists don't show asset groups.

## Plugin dependencies for asset groups

Install the sn\_isa\_model plugin for using asset groups.

