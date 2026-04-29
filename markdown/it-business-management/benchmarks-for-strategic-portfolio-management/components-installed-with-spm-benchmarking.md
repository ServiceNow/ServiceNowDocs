---
title: Components installed with SPM Benchmarking
description: Several types of components are installed with activation of the SPM Benchmarks plugin, including tables, user roles, and scheduled jobs.
locale: en-US
release: australia
product: Benchmarks for Strategic Portfolio Management
classification: benchmarks-for-strategic-portfolio-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SPM Benchmarks reference, SPM Benchmarks, Strategic Portfolio Management]
---

# Components installed with SPM Benchmarking

Several types of components are installed with activation of the SPM Benchmarks plugin, including tables, user roles, and scheduled jobs.

## Roles installed

<table id="table_opr_tlh_bvb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Benchmarking admin

 \[sn\_bm\_client.benchmark\_admin\]

</td><td>

-   Set up Benchmarks from an instance
-   Opt in or out of the Benchmarks program
-   Enable, disable, or modify indicators \(including changing Performance Analytics indicator source, script, and conditions for those KPIs not requiring application-specific roles\)
-   Receive email notification when new aggregate monthly data is available
-   All functions of the Benchmarks viewer and Benchmarks recommendations roles

</td><td>

None

</td></tr><tr><td>

Benchmarking data viewer

 \[sn\_bm\_client.benchmark\_data\_viewer\]

</td><td>

-   View full benchmark reports in Service Portal
-   View data visualizations and drill-downs for analyzing trends \(not PA scorecards\)
-   Download visualizations
-   View industry category or size comparisons
-   Receive email notification when a new aggregate monthly benchmark score is available.

</td><td>

None

</td></tr></tbody>
</table>## Scheduled jobs installed

<table id="table_qpr_tlh_bvb"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

SPM Benchmark Agile Data Collection

</td><td>

Collects scores for indicators related to Agile Development 2.0, as specified in the **Relative start** and **Relative end** fields. The collection time is for a month based on the GMT timezone.

</td></tr><tr><td>

SPM Benchmark Data Collection

</td><td>

Collects scores for indicators related to APW and PPM, as specified in the **Relative start** and **Relative end** fields. The collection time is for a month based on the GMT timezone.

</td></tr></tbody>
</table>**Parent Topic:**[SPM Benchmarks reference](benchmarks-reference.md)

