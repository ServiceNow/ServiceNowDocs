---
title: Linear assets in Enterprise Asset Management
description: Expand your asset management portfolio and increase diversification by creating and managing linear assets.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Explore, Enterprise Asset Management, IT Asset Management]
---

# Linear assets in Enterprise Asset Management

Expand your asset management portfolio and increase diversification by creating and managing linear assets.

## Overview of linear assets

A linear asset is an asset that has a physical length or dimension, such as roads, railways, pipelines, power transmission lines, and telecommunication networks. These assets are often characterized by their linear topology, which means that they have a defined start point and end point, and can be represented as a sequence of interconnected segments or nodes. A segment is a specific linear asset section that is defined either by a start point and an end point or by a start point and a length.

**Note:** For more details on the terminology that is used for linear assets, see [Terminology for linear assets](../reference/terms-eam.md).

You can create and manage linear assets and segments using geographic \(geo\) maps. Geo maps are integrated into the Enterprise Asset Management application.

## Extent of support for linear assets

Linear assets are supported keeping the following considerations in mind:

-   Support for linear assets that are modeled by geopoints.
-   Support for signed decimal degree geopoints up to seven digits after the decimal point. For example \[37.3800091, -121.9635865\].
-   Support for each linear asset extends to up to 1000 geopoints, 500 markers, and 500 segments.
-   Support for up to 1000 work orders on a linear asset per month.

## Geo maps for linear assets

Geo maps are visual representations of the Earth's surface or a specific region, displaying various features such as landforms, bodies of water, cities, roads, and other geographical elements.

sn-geo-map is the UI component used to support the map visualization in linear assets.

The Enterprise Asset Manager \[sn\_eam.enterprise\_asset\_manager\] has access to the geo map.

A geo map helps you perform the following actions on the workspace:

-   Draw linear assets to define coordinates.
-   Pick up segment start and end markers.
-   Pick up markers for discrete assets.
-   View related assets such as discrete assets, overlapping assets, intersecting assets, continuing assets, and segments.

For more information on using the Geomap icon to connect geo coordinate points on a map, watch this short video Connect geo coordinate points on a map

## Discreet asset relationships

You can associate your linear assets with discreet assets, which are enterprise assets and consumables that exist at specific points along a linear asset. For example, a pressure valve is a discreet asset that is placed at specific intervals along a pipeline. These associations enable you to track and manage your discreet assets as part of your linear assets.

You must assign each discreet asset a marker, which is a specific point location that falls within the boundary width of the associated linear asset. You can use this information to locate and query each discreet asset through the associated linear asset.

For more information on discreet assets, see [Associate a discrete asset to a linear asset](../task/associate-discreet-asset.md).

## Linear asset relationships

You can locate and identify the following relationships between your linear assets so that you can associate those assets with each other:

-   Overlapping linear assets: Assets that are in close proximity of each other and fall within the same boundary width. For example, a northbound and southbound highway.
-   Continuing linear assets: Assets that connect to each other at their start points and end points. When you reach the end point of one asset, you automatically transition into the start point of another asset. For example, a highway that changes into another highway after a specific point.
-   Intersecting linear assets: Assets that intersect at a specific point. For example, intersecting roads that meet or cross each other.

For more information on linear asset relationships, see [Find linear asset relationships](../task/find-linear-asset-relships.md).

