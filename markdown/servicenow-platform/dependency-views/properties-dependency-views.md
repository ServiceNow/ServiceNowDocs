---
title: Properties for Dependency Views
description: Use Dependency Views properties to configure how data appears in Dependency Views maps.
locale: en-US
release: australia
product: Dependency Views
classification: dependency-views
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Dependency Views, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Properties for Dependency Views

Use Dependency Views properties to configure how data appears in Dependency Views maps.

These properties are available for Dependency Views. To view and edit these properties, the sn\_cmdb\_admin or admin role is required.

<table id="table_vb2_wj3_rt"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Maximum number of CIs to display on a map at once.

 glide.bsm.max\_nodes

</td><td>

The maximum number of nodes to retrieve from the database. If more nodes exist in the database, they are not displayed in the map.

 -   Type: Integer
-   Default value: 1000
-   Location: **Dependency Views** &gt; **Map Properties**

</td></tr><tr><td>

Maximum level depth from the root CI that can be initially displayed in Dependency Views.

 glide.bsm.max\_levels

</td><td>

Level depth is the graph distance between the root CI and a node.

 -   Type: Integer
-   Default value:: 3
-   **Other possible values**: 1-49
-   Location: **Dependency Views** &gt; **Map Properties**

</td></tr><tr><td>

Display the continuation of the map underneath virtual group. Virtual links are used to connect virtual groups to their child nodes.

 glide.bsm.show\_virtual\_node\_children

</td><td>

-   Type: Yes \| No
-   Default value: No
-   Location: **Dependency Views** &gt; **Map Properties**

</td></tr><tr><td>

Maximum number of child nodes to display \(the rest will be collapsed\).

 glide.bsm.too\_many\_children

</td><td>

Maximum number of nodes \(of a similar CI type and at the same level\) to display before applying virtual grouping.Nodes are collapsed for the map to meet this limit.

 -   Type: Integer, valid values 1 or greater
-   Default value: 10
-   Location: **Dependency Views** &gt; **Map Properties**

</td></tr><tr><td>

A value of true indicates that filtered out items will be removed from the graph along with any disconnected children while a value of false indicates that the items will be dimmed in color.

 glide.ngbsm.filters\_remove\_filtered\_items

</td><td>

-   Type: Yes \| No
-   Default value: Yes
-   Location: **Dependency Views** &gt; **Map Properties**

</td></tr><tr><td>

Maximum number of relations per node.

 glide.bsm.max\_num\_rels

</td><td>

The maximum number of relations to retrieve from the database. If more relations exist in the database, they are not displayed in the map.

 -   Type: Integer
-   Default value: 100
-   Other values: 1 or greater
-   Location: **Dependency Views** &gt; **Map Properties**

</td></tr><tr><td>

A value of true indicates that when filters are changed the graph will recalculate it layout using the currently selected layout algorithm.

 glide.ngbsm.filters\_run\_layout\_automatically

</td><td>

-   Type: Yes \| No
-   Default value: Yes
-   Location: **Dependency Views** &gt; **Map Properties**

</td></tr><tr><td>

A value of true indicates that when filters are changed the graph will be fit to the screen automatically.

 glide.ngbsm.filters\_fit\_to\_screen\_automatically

</td><td>

-   Type: Yes \| No
-   Default value: No
-   Location: **Dependency Views** &gt; **Map Properties**

</td></tr><tr><td>

A value of true allows relationship lines to be drawn using smooth curves instead of straight line segments. These curves can be more taxing on the browser, setting to false may improve fluidity of animation and interaction for Dependency Views.

 glide.ngbsm.performance\_allow\_curves

</td><td>

-   Type: Yes \| No
-   Default value: Yes
-   Location: **Dependency Views** &gt; **Map Properties**

</td></tr><tr><td>

Amount of time in milliseconds a notification stays on the screen.

 glide.ngbsm.notification\_display\_time

</td><td>

-   Type: Integer
-   Default value: 5000
-   Location: **Dependency Views** &gt; **Map Properties**

</td></tr><tr><td>

The maximum amount of results displayed when searching for CIs.

 glide.ngbsm.search\_ci\_limit

</td><td>

-   Type: Integer
-   Default value: 10
-   Location: **Dependency Views** &gt; **Map Properties**

</td></tr><tr><td>

The maximum amount of results displayed when searching for Relationship Types.

 glide.ngbsm.search\_rel\_type\_limit

</td><td>

-   Type: Integer
-   Default value: 5
-   Location: **Dependency Views** &gt; **Map Properties**

</td></tr><tr><td>

When available, the map should display the class labels for each CI.

 glide.ngbsm.show\_class\_labels

</td><td>

-   Type: Yes \| No
-   Default value: Yes
-   Location: **Dependency Views** &gt; **Map Properties**

</td></tr><tr><td>

Truncate node labels to a single line and to fit available space \(default\). Disable to display entire labels on multiple lines and wrapped as needed.

 glide.ngbsm.truncate\_long\_labels

</td><td>

If **glide.ngbsm.show\_class\_labels** is enabled, then the class label always displays on top of the CI label, and wrapping applies to both the class and the CI labels.

 -   Type: Yes \| No
-   Default value: No
-   Location: **Dependency Views** &gt; **Map Properties**

</td></tr><tr><td>

Minimum horizontal distance between nodes in horizontal layout.

 glide.bsm.layout\_horizontal\_spacing\_x

</td><td>

The distance is measured in pixels between one node's center to another node's center.

 -   Type: Integer
-   Default value: 200
-   Location: **Dependency Views** &gt; **Map Properties**

</td></tr><tr><td>

Minimum vertical distance between nodes in horizontal layout.

 glide.bsm.layout\_horizontal\_spacing\_y

</td><td>

The distance is measured in pixels between one node's center to another node's center.

 -   Type: Integer
-   Default value: 100
-   Location: **Dependency Views** &gt; **Map Properties**

</td></tr><tr><td>

Minimum horizontal distance between nodes in vertical layout.

 glide.bsm.layout\_vertical\_spacing\_x

</td><td>

The distance is measured in pixels between one node's center to another node's center.

 -   Type: Integer
-   Default value: 125
-   Location: **Dependency Views** &gt; **Map Properties**

</td></tr><tr><td>

Minimum vertical distance between nodes in vertical layout.

 glide.bsm.layout\_vertical\_spacing\_y

</td><td>

The distance is measured in pixels between one node's center to another node's center.

 -   Type: Integer
-   Default value: 125
-   Location: **Dependency Views** &gt; **Map Properties**

</td></tr></tbody>
</table>