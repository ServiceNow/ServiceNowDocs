---
title: Asset groups in Enterprise Asset Management
description: Asset groups in the Enterprise Asset Management application provide a systematic approach to organizing assets based on their functional relationships and their physical placement within an organization. They can help improve data integrity and support maintenance planning, life-cycle tracking, reporting, and access control.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/enterprise-asset-management/asset-groups-eam.html
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Enterprise Asset Management data model, Explore, Enterprise Asset Management, IT Asset Management]
---

# Asset groups in Enterprise Asset Management

Asset groups in the Enterprise Asset Management application provide a systematic approach to organizing assets based on their functional relationships and their physical placement within an organization. They can help improve data integrity and support maintenance planning, life-cycle tracking, reporting, and access control.

## Organization of assets in Enterprise Asset Management

In the Enterprise Asset Management application, assets are organized through the following hierarchy types:

-   Location hierarchy: Hierarchy that defines the physical locations of your assets, organized based on the real-world location structure of those assets. This hierarchy enables location-based filtering, maintenance routing, and reporting.
-   Asset groups: Logical groupings of related assets and subgroups. Each asset group represents a functional system, process, or department within your organization.
-   Asset structure: Hierarchy that defines the parent-child relationships between assets. This hierarchy can help you complete work on your assets, plan spare parts, and track your asset life cycles.

## Overview of asset groups

An asset group is a logical grouping of assets. Each asset group can have multiple subgroups; however, a subgroup can belong to only one asset group. An asset can belong to multiple groups.

For details on creating asset groups and subgroups, see [Create an asset group in Enterprise Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/create-asset-groups-eam.md) and [Create an asset subgroup in Enterprise Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/create-asset-subgroup-eam.md). For details on adding assets to asset groups, see [Add assets to an asset group or subgroup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/add-assets-assetgroups.md).

**Note:** A subgroup inherits some fields from its parent group. For details on the fields that get inherited, see [Fields inherited from a parent asset group to a sub group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/subgroups-parent-fields-eam.md).

## Sites in asset groups

A site is an ISA-95 hierarchical entity model. Sites are organized in a hierarchical structure, with site being the top-level entity, followed by area, work center, and work unit.

You can associate an asset group to a site. This association enables all CIs that are associated with that specific site to also associate with the asset group.

**Note:** Only assets from the associated site and its specific location can be added to the asset group.

For details on creating sites, see [Create a site in the Enterprise Asset Management application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/create-sites-eam.md).

## Service instances and asset groups

An asset group or subgroup can optionally reference a service instance to pull all related assets from a chosen node in the given CI hierarchy. A subgroup can reference a service instance only if its parent group references one.

## Considerations for asset groups

Keep the following considerations in mind for asset groups:

-   An asset group can’t contain itself as a subgroup.
-   An asset group can’t have a model or model category, as it's a separate entity.
-   An asset group can't be deleted if it contains subgroups or assets. To delete an asset group, the sn\_eam.enterprise\_asset\_manager or the sn\_eam.enterprise\_admin role must first remove any subgroups and assets from the asset group.

## Considerations for adding assets to asset groups

Keep the following considerations in mind while adding assets to asset groups:

-   You can add only assets without a parent.​
-   You can add only hardware and enterprise assets. You can't add any consumable assets, linear assets, linear segments, or pallet assets.
-   Assets must be in the same location as the asset group or in a descendent location.
-   Asset must be in the In use or In maintenance state.​​

## Considerations for asset groups in Enterprise Asset Management flows and capabilities

Asset groups are unavailable in the following Enterprise Asset Management flows and capabilities:

-   Asset resale flow
-   Transfer order line management
-   Repair order line management
-   Disposal order management
-   Shipment asset creation
-   Contract management
-   Move order management
-   Any flow where the asset requires a model

## Plugin dependencies for asset groups

Asset groups require the sn\_isa\_model plugin, which is automatically installed with the Enterprise Asset Management application.

**Parent Topic:**[Enterprise Asset Management data model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/eam-data-model.md)

