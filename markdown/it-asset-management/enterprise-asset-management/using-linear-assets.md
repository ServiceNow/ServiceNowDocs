---
title: Linear assets in Enterprise Asset Management
description: Expand your asset management portfolio by creating and managing linear assets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/enterprise-asset-management/using-linear-assets.html
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Enterprise Asset Management data model, Explore, Enterprise Asset Management, IT Asset Management]
---

# Linear assets in Enterprise Asset Management

Expand your asset management portfolio by creating and managing linear assets.

## Overview of linear assets

A linear asset is an asset that has a physical length or dimension, such as roads, railways, pipelines, power transmission lines, and telecommunication networks. Each linear asset has a defined start point and end point and can be represented as a sequence of interconnected segments or nodes. A segment is a specific linear asset section that is defined either by a start point and an end point or by a start point and a length.

**Note:** For more details on the terminology that is used for linear assets, see [Terminology for linear assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/terms-eam.md).

**Note:** You can classify and manage linear assets by using the Linear asset \[sn\_eam\_linear\_asset\] class. This class extends the Enterprise asset \[sn\_ent\_asset\] class.

If a linear asset is divided into segments, you can classify and manage those segments by using the Linear segments \[sn\_eam\_linear\_segment\] class. This class extends the Linear asset \[sn\_eam\_linear\_asset\] class.

These classes are available only through the Expanded Model and Asset Classes application. For more information on this application, see [Enterprise model and asset classes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/enterprise-model-asset-classes.md).

## Geo maps for linear assets

You can create and manage linear assets and segments using geographic \(geo\) maps. Geo maps are visual representations of geographical areas, displaying geographical elements such as landforms, bodies of water, cities, and roads.

The Enterprise Asset Management application uses the sn-geo-map UI component to power map visualizations for linear assets. Only users with the Enterprise Asset Manager \(sn\_eam.enterprise\_asset\_manager\) role can access geo maps.

Geo maps help you perform the following actions in the Enterprise Asset Workspace:

-   Draw linear assets to define coordinates.
-   Set segment start and end markers.
-   Set markers for discrete assets.
-   View related assets such as overlapping assets, intersecting assets, and continuing assets.

## Discreet asset relationships

You can associate your linear assets with discreet assets, which are enterprise assets and consumables that exist at specific points along a linear asset. For example, a pressure valve is a discreet asset that is installed at regular intervals along a pipeline. These associations enable you to track and manage your discreet assets as part of your linear assets.

You must assign each discreet asset a marker, which is a specific point location that falls within the boundary width of the associated linear asset. You can use this information to locate and query each discreet asset through the associated linear asset.

For more information on discreet assets, see [Associate a discrete asset to a linear asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/associate-discreet-asset.md).

## Linear asset relationships

The Enterprise Asset Management application supports the following linear asset relationships:

-   **Overlapping linear assets**

    Assets that are in close proximity of each other and fall within the same boundary width. For example, a northbound and southbound highway running alongside each other.

-   **Continuing linear assets**

    Assets that connect to each other at their start points and end points. When you reach the end point of one asset, you automatically transition into the start point of another asset. For example, a highway that changes into another highway after a specific point.

-   **Intersecting linear assets**

    Assets that cross each other at a specific point. For example, two roads that cross each other at an intersection.


For more information on linear asset relationships, see [Find linear asset relationships](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/find-linear-asset-relships.md).

**Parent Topic:**[Enterprise Asset Management data model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/eam-data-model.md)

