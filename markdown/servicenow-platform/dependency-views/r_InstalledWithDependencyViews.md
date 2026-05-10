---
title: Components installed with Dependency Views
description: Several types of components are installed with the activation of the Next\_Gen BSM \(com.snc.ng\_bsm\) plugin, such as tables.
locale: en-US
release: australia
product: Dependency Views
classification: dependency-views
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Dependency Views, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Components installed with Dependency Views

Several types of components are installed with the activation of the Next\_Gen BSM \(com.snc.ng\_bsm\) plugin, such as tables.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/find-components.md).

## Tables installed

<table id="table_pqz_pj3_rt"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Available CI icons\[ngbsm\_ci\_icons\]

</td><td>

Stores all available CI class icons.

</td></tr><tr><td>

Icons for CI types\[ngbsm\_ci\_type\_icon\]

</td><td>

Maps icons to CI class names.

</td></tr><tr><td>

Map Script\[ngbsm\_script\]

</td><td>

Custom scripts that run in real time and generate a custom view of a map for a specific CI.

</td></tr><tr><td>

Map View \[ngbsm\_view\]

</td><td>

Serialized map views saved by users.

</td></tr><tr><td>

Map Filter \[ngbsm\_filter\]

</td><td>

Filters saved by users.

</td></tr><tr><td>

Menu Action \[ngbsm\_context\_menu\]

</td><td>

Default and custom context menu actions that appear when users right click a map.

</td></tr><tr><td>

Related Item \[ngbsm\_related\_item\]

</td><td>

Stores which reference fields should be treated as relationships when building the map. This allows users to include CI's that are related via a reference field instead of a relationship.

</td></tr><tr><td>

Edge Colors \[bsm\_edge\_color\]

</td><td>

Color definitions to use when drawing the relationships between nodes based on relationship type.

</td></tr><tr><td>

Map Indicator\[bsm\_indicator\]

</td><td>

Stores all map indicators.

</td></tr><tr><td>

BSM Saved Map\[bsm\_graph\]

</td><td>

Details of maps.

</td></tr><tr><td>

BSM Map Actions \[bsm\_action\]

</td><td>

Actions on the map.

</td></tr><tr><td>

BSM Map View\[map\_view\]

</td><td>

Parents' predefined filters.

</td></tr><tr><td>

Map View Configuration Types\[map\_view\_ci\_type\]

</td><td>

Configuration type filters, limiting the CI class types to be displayed, per predefined filter.

</td></tr><tr><td>

Map View Relationship Types\[map\_view\_rel\_type\]

</td><td>

Relationship type filters, limiting the links to be displayed between CIs, per each predefined filter.

</td></tr><tr><td>

\[map\_viewroles\]

</td><td>

Roles that a specific predefined filter should be applied to.

</td></tr><tr><td>

CI Filters\[map\_filters\]

</td><td>

CI attribute filters, limiting the CIs to be displayed, per predefined filter.

</td></tr></tbody>
</table>