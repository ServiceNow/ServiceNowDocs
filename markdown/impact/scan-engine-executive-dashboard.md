---
title: Scan Engine Executive dashboard
description: The Executive dashboard includes trend charts and the following overview modules.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Analytics Dashboards, Scan Engine, Platform Health, Using Impact, Impact]
---

# Scan Engine Executive dashboard

The Executive dashboard includes trend charts and the following overview modules.

<table id="table_afw_4vz_chc"><thead><tr><th>

Information module

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Outstanding technical debt

</td><td>

-   The total time required to resolve existing technical debt on your platform, based on the effort of a single developer.  It does not include time for testing, validation, or other stages of the software development life-cycle \(SDLC\).
-   The graph line shows the trend of technical debt over a certain time period.
-   The time period shown depends on available data, with a maximum of 90 days of information displayed.

</td></tr><tr><td>

Technical debt prevented

</td><td>

-   Reflects the amount of technical debt prevented from entering the instance because of the Scan Engine’s real-time prevention.
-   The graph line shows the trend of technical debt prevented over the past month.

</td></tr><tr><td>

Health score

</td><td>

The health score represents the percentage of definition occurrences used across the platform that did not return any findings. It is calculated as:

 `1 - (F / D) * 100`

 Where F is the number of findings, and D is the number of definition occurrences.

 "Definition occurrences" refers to the total number of times a definition has been executed by the Scan Engine to generate findings.

</td></tr><tr><td>

Health score thresholds

</td><td>

-   90-100% = Excellent
-   80-89% = Good
-   70-79% = Fair
-   Below 70% = At risk

</td></tr><tr><td>

Findings resolved by proposed fix

</td><td>

The number of findings resolved using the proposed fix feature. **Note:** This feature is only available to ServiceNow customers who have purchased the Impact Total package or the Platform Health add-on.

</td></tr><tr><td>

Findings by categories

</td><td>

-   The estimated amount of development cost required to resolve all findings within each category.
-   The value shown in the center is the combined total finding of cost, time, or count for all categories

</td></tr><tr><td>

Active definitions

</td><td>

The definitions used to determine violations with the Scan Engine.

</td></tr><tr><td>

Findings resolved by AI

</td><td>

The number of findings resolved using the Code Fix AI Agent feature.**Note:** This feature is only available to ProPlus customers.

</td></tr></tbody>
</table>## Executive dashboard trend charts

The Executive dashboard includes the following trend charts.

<table id="table_zwq_yhl_fhc"><thead><tr><th>

Chart

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Outstanding technical debt

</td><td>

-   The amount of development time required to resolve all findings.
-   You can customize the time period using the date selector.

</td></tr><tr><td>

Health score

</td><td>

The percentage of scanned definitions that returned zero findings. This is calculated as:`1 - (F / D) * 100`

Where F is the number of findings, and D is the number of definition occurrences.

</td></tr><tr><td>

Outstanding findings

</td><td>

The trend of all findings found during the scheduled instance scan.

</td></tr><tr><td>

Total impact to instance

</td><td>

-   The total impact to instances, derived from the sum of the scheduled scan findings over the selected time period.
-   Represents the impact of your findings to your instance when a finding is not resolved.
-   You can customize the time period using the date selector.

</td></tr><tr><td>

Real-time preventions

</td><td>

-   The sum of real-time preventions over the selected time period.
-   A real-time prevention is when the Scan Engine prevents a finding from being saved.
-   You can customize the time period using the date selector.

</td></tr><tr><td>

Total resolved findings

</td><td>

-   The trends for all resolved findings found from nightly instance scanning over the selected time period.
-   You can customize the time period using the date selector.
-   You can select one of the following display options:
    -   **All resolved findings**
    -   **Findings by proposed fix applied**
    -   **Findings that were resolved manually**

 **Note:** The Scan Engine property **Track resolved findings** must be active to populate this chart. See [Configure Scan Engine properties](../task/configure-scan-engine-properties.md).

</td></tr><tr><td>

Instance comparison

</td><td>

A side-by-side comparison of the technical debt for all instances in the My SN Instances table. Technical debt is broken down by category to quickly view differences between environments.

</td></tr></tbody>
</table>## Executive dashboard data sources

The following tables show the data source for each overview and trend chart in the Executive dashboard.

**Note:** All components require either the impact.admin or impact.executive role to use.

|Component|Data Source|
|---------|-----------|
|Outstanding technical debt|sn\_se\_summary\_scan\_detail|
|Technical debt prevented|sn\_se\_onsubmit\_prevention|
|Health score|sn\_se\_scan\_result|
|Findings resolved by proposed fix|sn\_se\_resolved\_finding\_history|
|Findings by categories|sn\_se\_summary\_scan\_detail|
|Active definitions|sn\_se\_definition|
|Codefix AI agent|sn\_impact\_code\_remediation\_suggestion\_item|
|Outstanding findings|sn\_se\_summary\_scan\_detail|
|Definition occurrences|sn\_se\_scan\_result|

| | |
|---|---|
|Outstanding technical debt|sn\_se\_summary\_scan\_detail|
|Health score|sn\_se\_scan\_result|
|Outstanding findings|sn\_se\_scan\_result|
|Total impact to instance|sn\_se\_scan\_result|
|Real time preventions|sn\_se\_onsubmit\_prevention|
|Total resolved findings|sn\_se\_scan\_result|
|Instance comparison|sn\_se\_my\_sn\_instances|

**Note:** `sn_se_scan_result` and `sn_se_summary_scan_detail` are populated from the latest full scan or delta scan, the values are updated after the scan is completed.

