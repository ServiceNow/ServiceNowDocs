---
title: Evaluate the performance of a portal page
description: Evaluate how the widgets on a page perform against performance benchmarks that you specify.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Analyzing portal performance and usage, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Evaluate the performance of a portal page

Evaluate how the widgets on a page perform against performance benchmarks that you specify.

## Before you begin

Role required: sp\_admin or admin

## Procedure

1.  Turn on the Performance Analyzer for the portals that you want to evaluate.

    By default, the Performance Analyzer is enabled for the Service Portal \(sp\).

    1.  In the navigation filter, enter `sys_properties.list`.

    2.  Filter the list by entering **sp\_allow\_perf\_debug\_option\_for\_portals** for the Name field.

    3.  Select the **sp\_allow\_perf\_debug\_option\_for\_portals** record.

    4.  In the Value field, enter the suffixes of the portals to analyze.

    For users with the sp\_admin or admin roles, the open Performance Analyzer icon \(![Open Performance Analyzer icon.](../image/performance-analyzer-icon.png)\) appears on pages in the specified portals.

2.  Navigate to the portal page that you want to analyze.

3.  Select the open Performance Analyzer icon \(![Open Performance Analyzer icon.](../image/performance-analyzer-icon.png)\).

    The Performance Analyzer opens in another browser tab. The Portal Page URL field automatically populates with the URL of the page from which you open the Performance Analyzer.

4.  From the Benchmarks details tab, enter the performance benchmarks to analyze the page against.

    |Benchmark|Description|
    |---------|-----------|
    |Widget Load Time \(ms\)|The time, in milliseconds \(ms\), that it takes for a widget to load on the page.|
    |ACL Execution time \(ms\)|The time, in milliseconds \(ms\), that it takes for a widget to execute any applicable ACLs.|
    |DB Call Execution Time \(ms\)|The time, in milliseconds \(ms\), that it takes for a widget to execute database queries.|
    |Business Rule Execution Time \(ms\)|The time, in milliseconds \(ms\), that it takes for a widget to execute business rules.|
    |Ajax Calls Time \(ms\)|The time, in milliseconds \(ms\), that it takes for a widget to execute AJAX calls.|
    |Ajax Waiting Time \(sec\)|The time, in seconds \(s\), to wait for AJAX calls after the page has finished loading.|

5.  Select **Validate**.

    **Note:** During validation, refrain from interacting with other pages on the instance as doing so could impact the results of the page evaluation.

    The Performance Analyzer returns the benchmark results, which include any widgets on the page that exceed the benchmarks and details about their performance.

6.  Review the benchmark results.

<table id="choicetable_drv_ynr_jdc"><thead><tr><th align="left" id="d58522e237">

Option

</th><th align="left" id="d58522e240">

Steps

</th></tr></thead><tbody><tr><td id="d58522e246">

**Benchmark details**

</td><td>

From the Benchmark results list, select a widget or AJAX API to view additional details about its ACLs, business rules, or database calls.

 ![Performance results for each widget on the page from the Benchmark details view](../image/performance-analyzerbenchmark-details.png)

</td></tr><tr><td id="d58522e265">

**Preview**

</td><td>

1.  Select **Show preview**.

Any widgets on the page that exceed the specified benchmarks are highlighted on the page.

2.  Select the information icon \(![Information icon.](../../../administer/workspace/image/icon-information.png)\) for a highlighted widget to view its benchmark results.

![A widget's performance results from the Preview view](../image/performance-analyzer-preview.png)

</td></tr></tbody>
</table>7.  To evaluate the page against different benchmarks, select **Start Over** and enter new benchmarks.


## What to do next

Consider updating any widgets that don’t meet your performance benchmarks to improve the page performance. For example, if a widget's server script takes too long to load, evaluate if the script can be improved to load faster.

**Parent Topic:**[Analyzing portal performance and usage](../concept/using-portal-analytics.md)

