---
title: Linear assets in Enterprise Asset Management
description: Use linear assets to expand your asset management portfolio and increase diversification by creating and managing linear assets.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Explore, Enterprise Asset Management, IT Asset Management]
---

# Linear assets in Enterprise Asset Management

Use linear assets to expand your asset management portfolio and increase diversification by creating and managing linear assets.

## Overview of linear assets

A linear asset is an asset that has a physical length or dimension, such as roads, railways, pipelines, power transmission lines, and telecommunication networks. These assets are often characterized by their linear topology, which means that they have a defined starting point and ending point, and can be represented as a sequence of interconnected segments or nodes.

You can create segments on linear assets, associate discreet asset to linear assets, and find relationships between linear assets such as overlapping assets, continuing assets, and intersecting assets. For details on the terminology used for linear assets, see [Terminology for linear assets](../reference/terms-eam.md).

You can create and manage linear assets and segments using geographic \(geo\) maps. Geo maps are integrated into the Enterprise Asset Management.

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

