---
title: Link an automated indicator to a benchmark
description: To enable the comparison of indicators to ITSM and ITOM benchmarks, link an automated indicator to the corresponding benchmark KPI. A benchmark KPI can be linked to only one indicator. You can compare the linked indicators in the Analytics Hub.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Indicators, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Link an automated indicator to a benchmark

To enable the comparison of indicators to ITSM and ITOM benchmarks, link an automated indicator to the corresponding benchmark KPI. A benchmark KPI can be linked to only one indicator. You can compare the linked indicators in the Analytics Hub.

## Before you begin

You must opt-in to the ServiceNow® Benchmarks application.

Role required: pa\_data\_collector, pa\_power\_user, admin

**Note:** If you have the sn\_bm\_client.benchmark\_admin role, you can link Performance Analytics indicators to benchmark indicators through the Benchmarks Setup interface. For instructions about linking indicators through that interface, see [Link or customize a benchmark KPI](https://www.servicenow.com/docs/access?context=t_CustomBenchKPIConditions&version=australia&pubname=australia-it-service-management&ft:locale=en-US).

## About this task

Used together, benchmarking and Performance Analytics enables you to measure your enterprise ITSM and ITOM against industry standards while driving improvements across all important metrics. For more information, see [Benchmarks](https://www.servicenow.com/docs/access?context=benchmarks-landing&version=australia&pubname=australia-it-service-management&ft:locale=en-US).

## Procedure

1.  In the list of [automated indicators](../concept/performance-analytics-glossary.md#) or the list of formula indicators, identify which benchmark indicator you want to link to which other indicator.

    Benchmark indicator names begin with the word **Benchmark**.

2.  Verify that the benchmark indicator and the linked indicator are configured compatibly.

    Specifically, verify that the following properties match in both indicators:

    -   Indicator source
    -   Unit
    -   Formula \(for formula indicators\)
    **Warning:** The indicators in Platform Analytics Solutions are not configured the same as the matching benchmark indicators.

3.  Open the benchmark indicator record.

4.  In the **Linked indicator** field under **Indicator properties**, select the automated indicator to link to the benchmark.

    **Note:**

    -   The fully licensed version of Performance Analytics must be activated to see the complete list of Performance Analytics automated and formula indicators.
    -   To edit the **Linked indicator** field, you may need to change the scoped application that you are working in, at the top of the record.
    -   The names of the benchmark indicator and the indicator to link might not match.

## Result

After you update the benchmark KPI record, you can compare the benchmark KPI and the automated indicator on the **Compare** tab of the Analytics Hub for the automated indicator. For more information and an example, see [Compare scores](../concept/scorecard-compare-tab.md).

