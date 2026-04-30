---
title: Create linear assets
description: Create linear assets to diversify your Enterprise Asset Management portfolio.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Create and manage enterprise assets, Managing enterprise assets and models, Enterprise Asset Management, IT Asset Management]
---

# Create linear assets

Create linear assets to diversify your Enterprise Asset Management portfolio.

## Before you begin

Role required: sn\_eam.enterprise\_asset\_manager

## Procedure

1.  Navigate to **Enterprise asset estate** &gt; **Linear assets**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="choicetable_qqz_vqx_kxb"><thead><tr><th align="left" id="d107569e77">

Field

</th><th align="left" id="d107569e80">

Description

</th></tr></thead><tbody><tr><td id="d107569e86">

**Name**

</td><td>

Unique name of the linear asset.

</td></tr><tr><td id="d107569e95">

**Linear asset type**

</td><td>

Type of the linear asset. Select from the list or you can create your own asset type.

</td></tr><tr><td id="d107569e104">

**Description**

</td><td>

Description of the linear asset.

</td></tr><tr><td id="d107569e113">

**Location**

</td><td>

Vicinity of your linear asset. To draw a linear asset, select the Geomap icon to display the map. After you enter the location, the map will properly focus and zoom to that vicinity.For more information on using the Geomap icon to connect geo coordinate points on a map, watch this short video Connect geo coordinate points on a map

</td></tr><tr><td id="d107569e130">

**Boundary width**

</td><td>

Boundary width of the linear asset.

 The boundary width helps in associating discrete assets with linear assets. The discrete asset's location must fall within the linear asset's boundary widths. For example, if the boundary width of a linear asset is 500 feet, a discrete asset can be associated to it only if the discrete asset is within 250 feet of that linear asset.

</td></tr><tr><td id="d107569e145">

**Width unit**

</td><td>

The width of the linear asset in units.

</td></tr><tr><td id="d107569e154">

**Length unit**

</td><td>

The unit the length of the linear asset is measured in.

</td></tr><tr><td id="d107569e163">

**Length**

</td><td>

The length of the linear asset. This input field is optional. If it isn’t filled out, it’s calculated using the coordinates.

</td></tr><tr><td id="d107569e172">

**Start marker**

</td><td>

The start point of the linear asset.

</td></tr><tr><td id="d107569e181">

**End marker**

</td><td>

The end point of the linear asset.

</td></tr><tr><td id="d107569e191">

**Coordinates**

</td><td>

A list of two or more geographical \(geo\) points. Each geo point has a latitude and longitude. For example, \[\[37.377323, -121.961947\], \[37.380582, -121.976565\]\].

 If you already have the linear asset's coordinates, you can paste them into this field. Otherwise, you can use the Geomap icon in the **Attachments**section to draw the geo points on a map.

 The start marker and the end marker are created based on the first and the last coordinates. Markers are common location records associated with the Geolocation type. In the common location hierarchy, all markers of a linear asset are placed under Vicinity Geolocation, which is under Vicinity. Vicinity refers to the location of the linear asset.

</td></tr></tbody>
</table>4.  Select **Save**.

    The linear asset is created and appears in the Linear assets list. You can perform additional configuration on the linear asset by entering details in the other related lists such as **Linear segments**, **Discreet assets**, **Related linear assets**, **Contracts**, and **Expense lines**.


**Parent Topic:**[Create and manage enterprise assets](../concept/create-manage-enterprise-assets.md)

