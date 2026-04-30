---
title: Troubleshoot a slow pattern
description: Identify the source of a slow pattern and prioritize potential performance improvements.
locale: en-US
release: zurich
product: Platform Performance
classification: platform-performance
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Solving slow patterns, Application Insights, Monitor, Platform performance, Maintain and monitor, Administer]
---

# Troubleshoot a slow pattern

Identify the source of a slow pattern and prioritize potential performance improvements.

## Before you begin

Role required: sn\_app\_insights.admin or admin

Starting with the Zurich release, Application Insights is no longer deployed, enhanced, or supported. It is recommended to evaluate the [Overview of Instance Observer](https://www.servicenow.com/docs/access?context=io-overview&version=zurich&pubname=zurich-impact&ft:locale=en-US) product available with the ServiceNow Impact packages. Work with your Account team to review Impact packages.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## Procedure

1.  Navigate to **All** &gt; **Application Insights** &gt; **Application Insights** &gt; **Slow Patterns**.

2.  Look for potential performance issues by viewing the Slow Events, Slow Transactions, Slow Queries, and Slow Scripts tables.

    -   Focus on a 1-day, 7-day, or 30-day period by selecting a day range.
    -   Identify patterns with consistently high execution times by sorting on the **Average execution time in range** column.
    -   Find out which patterns are executed the most often by sorting on the **Execution count in range** column.
3.  Select a slow pattern with a high execution time and high execution count.

    The **Average Execution Time** detail graph shows the slow pattern's execution time and its 1-day moving average.

4.  View the performance for the slow pattern over time by analyzing the **Average Execution Time** detail graph.

    -   Look for spikes within the selected time range. Look for correlations to impactful system events that might indicate a false alarm by overlaying diagnostic events.
    -   View the number of times the pattern was executed in the selected time range.
    -   Determine whether performance is worsening over time by viewing the direction of the 1-Day Moving Average trend line.
5.  Find out what is triggering the slow pattern by selecting **View Record**.

    The slow pattern record appears and provides additional details including the query or script contents, the first time it was executed, and the last time it was executed.

6.  To access additional helpful information for troubleshooting, add the Referenced Scripts and Related Slow Patterns related lists.

<table id="choicetable_f4t_kdp_cvb"><tbody><tr><td id="d187291e172">

**Slow scripts**

</td><td>

1.  Select the form context menu \(![Context menu icon](../../subscription-management/image/context-menu.png)\).
2.  Change the form view by selecting **View** &gt; **Slow Script Insights**.


</td></tr><tr><td id="d187291e202">

**Slow queries**

</td><td>

1.  Select the form context menu \(![Context menu icon](../../subscription-management/image/context-menu.png)\).
2.  Change the form view by selecting **View** &gt; **Slow Query Insights**.


</td></tr></tbody>
</table>7.  Determine the cause of the slowness.

    -   When investigating a slow query, determine which script or business rule triggered the slowness by finding the entry with the highest calling order in the Referenced scripts related list. For example, suppose a slow query is triggered by a script whose calling order is 2 that is called by a business rule whose calling order is 1. That script directly triggered the slow query because it has the highest calling order.
    -   When investigating a slow script, identify the slow patterns triggered by the script by viewing the patterns in the Related slow patterns related list. Determine which slow patterns to investigate first by sorting on the **Average Execution Time in Range** and **Average Execution Count in Range** columns. Investigate the slow patterns with the highest values in each column first.
    -   Confirm a potential issue by viewing the Related slow patterns list, which provides a list of other slow patterns that have referenced scripts in common. If multiple slow patterns reference the same script include or business rule, you can be confident that is where the issue lies.
8.  For troubleshooting multiple slow patterns, open each record, check the number of entries in the Related Slow Patterns related list, and prioritize debugging or resolving the slow pattern with the higher count.

    Debugging the slow pattern with the higher count is more likely to make a greater performance improvement.

9.  Take actions to solve the performance issue.

    -   Optimize or remove the offending script include or business rule.
    -   Determine whether you can avoid using the slow query. If the query is required, try to optimize it with additional query conditions or a sys\_id query so that it returns only the information that is needed.
    -   Determine whether an index can optimize the performance of the slow query.

**Parent Topic:**[Solving slow patterns](../concept/application-insights-slow-patterns.md)

