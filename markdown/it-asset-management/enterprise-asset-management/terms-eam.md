---
title: Terminology for linear assets
description: Terms commonly used for linear assets in the Enterprise Asset Management application.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [References, Enterprise Asset Management, IT Asset Management]
---

# Terminology for linear assets

Terms commonly used for linear assets in the Enterprise Asset Management application.

## Linear asset terms and their description

<table id="table_klw_32z_kxb"><thead><tr><th>

Term

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Linear asset

</td><td>

An asset that has a physical length or dimension, such as roads, railways, pipelines, and power transmission lines.

 Linear assets have a series of geopoints; at least a start and end point and have segments with different attributes.

</td></tr><tr><td>

Geo point

</td><td>

Geo points, or graphical coordinates, are a way of expressing a location on the earth's surface using a set of numerical values.

 Geo points consists of latitudes, longitudes, and altitudes and can be visualized on a map. In the Enterprise Asset Management application, geo point latitude and longitude refer to the coordinate format defined by WGS 84 and uses signed  decimal degrees.

</td></tr><tr><td>

Route

</td><td>

Geo points of a linear asset form a route. Routes can be plotted and visualized on a map.

</td></tr><tr><td>

Boundary width

</td><td>

Maximum width of the linear asset. It’s used to validate whether a cmn\_location is on-route or not.

</td></tr><tr><td>

Marker

</td><td>

A point location that can be identified on or near a linear asset. A marker should contain a geo point so it can be visualized on a map. If the geo point is on the route of the linear asset, then it’s an on-route marker.

</td></tr><tr><td>

Segment

</td><td>

A section of a linear asset with certain attributes. A segment consists of a start point and an end point, or a start point and length.

</td></tr><tr><td>

Discrete asset

</td><td>

Discrete assets are enterprise assets and consumables. Discrete assets can be associated to a linear asset and be managed as part of the linear asset.

</td></tr><tr><td>

Overlap asset

</td><td>

A linear asset relationship where two or more linear assets are in close proximity and within the boundary width. For example, a northbound and a southbound highway. A linear asset can be defined for a northbound highway and another linear asset for a southbound highway.

</td></tr><tr><td>

Intersect asset

</td><td>

A linear asset relationship where linear assets have an intersect point. For example, intersecting roads, where two or more roads meet or cross each other.

</td></tr><tr><td>

Continue asset

</td><td>

A linear asset relationship for linear assets that have a start and an end marker. For example, a highway that after a particular point changes into another highway.

</td></tr></tbody>
</table>**Parent Topic:**[Enterprise Asset Management reference](../concept/reference-enterprise-asset-management.md)

**Related topics**  


[Domain separation and Enterprise Asset Management](../concept/domain-separation-eam.md)

[Enterprise Asset Management roles](eam-roles.md)

[OT Asset Workspace roles](ot-workspace-roles.md)

[Asset fields for enterprise assets](asset-fields-eam.md)

[Asset audit fields for enterprise assets](asset-audit-record-fields-eam.md)

[Audit results](audit-results-eam.md)

[Enterprise model categories and corresponding classes](enterprise-model-categories.md)

[Mandatory fields in the bulk import spreadsheets](mandatory-bulk-fields.md)

[Normalization status for enterprise models](norm-status-eam.md)

[Model fields for Enterprise Asset Management](eam-model-fields.md)

[Contract fields for Enterprise Asset Management](contract-fields-eam.md)

[Maintenance plan fields for Enterprise Asset Management](maintenance-plan-fields-eam.md)

[Maintenance schedule fields for Enterprise Asset Management](maintenance-schedule-fields-eam.md)

[Work plan fields for Enterprise Asset Management](wp-fields-eam.md)

[Work plan schedule fields for Enterprise Asset Management](work-plan-schedule-fields-eam.md)

[Expense line fields for Enterprise Asset Management](expense-line-fields-eam.md)

[Fields inherited from a parent asset group to a sub group](subgroups-parent-fields-eam.md)

[Enterprise asset disposal order stages](eamasset-disposalorder-stages.md)

[Installed with Enterprise Asset Management for Healthcare](installed-with-eam-healthcare.md)

[Installed with OT Asset Management](installed-with-otam.md)

[Components installed with Enterprise Asset Management for Data Center and Network Asset Management \(DCNAM\)](installed-with-eam-dcnam.md)

[Components installed with Enterprise Asset Management for Providers](installed-with-eam-providers.md)

[Scheduled jobs and tables installed with normalization of firmware models](firmware-tables-jobs-ot.md)

[Asset put away task fields](put-away-task-form-eam.md)

