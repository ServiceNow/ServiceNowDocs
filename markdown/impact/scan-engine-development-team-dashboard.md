---
title: Scan Engine Developer dashboard
description: The Developer dashboard includes trend charts and the following overview modules.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-10-22"
reading_time_minutes: 1
breadcrumb: [Analytics Dashboards, Scan Engine, Platform Health, Using Impact, Impact]
---

# Scan Engine Developer dashboard

The Developer dashboard includes trend charts and the following overview modules.

<table id="table_qcw_zml_fhc"><thead><tr><th>

Information module

</th><th>

Description

</th></tr></thead><tbody><tr><td>

My open findings by impact to instance

</td><td>

-   A developer’s total findings grouped by impact to instance.
-   Impacts to instance range from 1 \(minor impact\) to 10 \(significant impact\).
-   Select a bar in the chart to view the findings in a new browser tab.

</td></tr><tr><td>

My technical debt by category

</td><td>

-   The estimated amount of development time required to resolve all findings within each category.
-   The value in the center is the combined total technical debt displayed in either time or count for all categories.

</td></tr></tbody>
</table>## Developer trend charts

The Developer dashboard includes the following trend charts.

<table id="table_wyf_jnl_fhc"><thead><tr><th>

Chart

</th><th>

Description

</th></tr></thead><tbody><tr><td>

My findings by priority

</td><td>

A developer’s assigned findings listed by highest impact to instance and lowest time to resolve. Address these findings to achieve the highest impact in return for the lowest effort.

</td></tr><tr><td>

Policy prioritized findings

</td><td>

-   A developer’s findings that have a Priority status within a policy.
-   Findings listed here were last updated by the developer.

</td></tr><tr><td>

My open findings

</td><td>

The current open findings that the Scan Engine has identified in a developer’s code.

</td></tr><tr><td>

My exceptions

</td><td>

The current exceptions a developer has submitted that require a Team Lead's approval.

</td></tr><tr><td>

My findings by file type

</td><td>

-   The heatmap of your findings by file type. This lets you quickly see which development areas need the most attention.
-   Select a number in any cell to see the full list of findings for that file type/category.

</td></tr><tr><td>

My resolved findings

</td><td>

Findings that have been resolved in a developer’s code.

</td></tr></tbody>
</table>## Developer dashboard data sources

The following tables show the data source for each overview module and trend chart in the Developer dashboard.

**Note:** All components require either the impact.admin or impact.developer role to use.

|Component|Data Source|
|---------|-----------|
|My open findings by impact to instance|sn\_se\_summary\_scan\_detail|
|My technical debt by category|sn\_se\_summary\_scan\_detail|

|Component|Data Source|
|---------|-----------|
|My open findings by priority|sn\_se\_finding|
|Policy prioritized findings|sn\_se\_finding|
|My open findings|sn\_se\_summary\_scan\_detail|
|My exceptions|sn\_se\_exception\_reason|
|My findings by file type|sn\_se\_summary\_scan\_detail|
|My resolved findings|sn\_se\_resolved\_finding\_history|

