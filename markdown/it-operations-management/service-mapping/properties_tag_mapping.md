---
title: Properties related to tag-based discovery
description: The Service Mapping plugin includes several properties specifically related to tag-based discovery.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service Mapping reference, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Properties related to tag-based discovery

The Service Mapping plugin includes several properties specifically related to tag-based discovery.

**Note:** To open the System Property \[sys\_properties\] table, enter `sys_properties.list`in the navigation filter.

<table id="table_gw2_vg1_fwb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_sm\_scoped\_app.svc\_by\_tags.max\_candidates\_per\_family

</td><td>

Limits the maximum number of tag-based service candidates created for a single family. If the family definition includes more candidates, the most recently updated CIs take precedence. This value applies to all tag-based service families.

-   **Type:** integer
-   **Default value:** 200

</td></tr><tr><td>

svc\_by\_tags.classes.whitelist

</td><td>

This property contains the list of allowed CI classes separated by commas. Tag-based mapping includes the CIs belonging to these classes. An empty ‘value’ field indicates the inclusion of all CI classes.

</td></tr><tr><td>

svc\_by\_tags.install\_status.blacklist

</td><td>

This property contains the list of exclusions based upon the install status separated by commas. Tag-based mapping excludes any tagged CIs with the following install statuses:**Note:** In this context, CIs brought by traversal rules are not considered tagged. This property applies only to original tagged CIs.

**Default value**: 7,100

 **Other possible values**:

 Installed=1, On order=2, In maintenance=3, Pending install=4, Pending repair=5, In stock=6, Retired=7, Stolen=8

</td></tr><tr><td>

svc\_by\_tags.max.categories.per.family

</td><td>

Set the maximum number of categories allowed per service family.-   **Type**: integer
-   **Default value**: 3

</td></tr><tr><td>

svc\_by\_tags.max.traversal.rules.active

</td><td>

Set the maximum allowed number of CI relationships that can be in the active state. Service Mapping uses only active CI relationships for tag-based discovery. -   **Type**: integer
-   **Default value**: 5
-   **Location**: System Property \[sys\_properties\] table

</td></tr><tr><td>

svc\_by\_tags.max\_ci\_limit

</td><td>

Set the maximum allowed number of CIs that a tag-based application service can contain.-   **Type**: integer
-   **Default value**: 1000
-   **Location**: System Property \[sys\_properties\] table

</td></tr></tbody>
</table>**Parent Topic:**[Service Mapping reference](service-mapping-reference.md)

