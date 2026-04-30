---
title: KPI Details UUIDs
description: Every combination of breakdowns, elements, a time series aggregation, and a domain that you specify for an indicator has a unique identifier \(UUID\). To understand how the KPI Details and KPI Signals applications work, you should understand how these UUIDs are constructed.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [KPI Details reference, KPI Details, Platform Analytics experience, Platform Analytics]
---

# KPI Details UUIDs

Every combination of breakdowns, elements, a time series aggregation, and a domain that you specify for an indicator has a unique identifier \(UUID\). To understand how the KPI Details and KPI Signals applications work, you should understand how these UUIDs are constructed.

In the Analytics Hub and the workspace KPI Details, you select an indicator and can specify it further by the following:

-   Up to two levels of breakdown
-   Element filter
-   Up to two levels of breakdown element, including multiple elements per level \(aggregate score\)
-   A time series aggregation
-   Domain separation

Each combination is represented by a so-called UUID. The UUID is concatenated from the sys\_IDs of the indicator and any of these specifiers, in the following order \(note the semicolon before the domain id\):

`&lt;indicator\_sys\_id&gt;:&lt;breakdown\_sys\_id&gt;:&lt;elements\_filter\_sys\_id or element\_sys\_ids&gt;:&lt;lvl-2 breakdown\_sys\_id&gt;:&lt;lvl-2 elements\_filter\_sys\_id or element\_sys\_ids&gt;:&lt;aggregate\_sys\_id&gt;;&lt;domain\_sys\_id&gt;`

All specifiers other than **indicator\_sys\_id** are optional, with one exception: If a **breakdown\_sys\_id** is specified, so must be at least one **element\_sys\_id**. To specify a breakdown and not specify elements, for example to get a list of all elements, the breakdown sys\_id goes in a separate parameter. For an example, see this [GET/now/pa/scorecards REST API example](../../../integrate/inbound-rest/reference/r_PerformanceAnalyticsAPIExamples.md). To refer to those scores that do not match any elements of the specified breakdown, the string `unmatched` goes in place of an **element\_sys\_id**.

Targets, thresholds, and other Analytics Hub and KPI Details functions apply per UUID. In other words, they apply separately to each unique combination of indicator, breakdowns, elements and element filters, time series aggregation, and domain. The KPI Signals application also monitors each fully specified indicator separately, per UUID.

**Parent Topic:**[KPI Details reference](kpi-details-reference.md)

