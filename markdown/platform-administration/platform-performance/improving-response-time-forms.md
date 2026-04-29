---
title: Improving response times on forms
description: Learn the techniques that can be used to improve form response times. If you notice latency or slow response times on forms, using these techniques can help improve performance.
locale: en-US
release: australia
product: Platform Performance
classification: platform-performance
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Resolve issues, Platform performance, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Improving response times on forms

Learn the techniques that can be used to improve form response times. If you notice latency or slow response times on forms, using these techniques can help improve performance.

1.  If you notice one or more transactions that span the entire form response time window, try adding additional indexing to the database to make the transaction faster. Even with indexing, some queries might still take longer than others.

    For more information about indexing, see [Resolving slow queries](resolving-slow-queries.md).

2.  Verify that a cache flush isn't being run during business hours.

    Cache flushes are intended to help prevent older data from interfering with changes and updates, and are performed automatically when using update sets. Scheduled cache flushes, using cache.do, can affect overall performance and degrade system response times. Don't run cache flushes or trigger automatic cache flushes during business hours.

    For more information about actions that trigger automatic cache flushes, see [Instance cache effects on performance](instance-cache-performance-effects.md).

3.  If you can't find any specific issues leading to slow response times on forms, contact Customer Service and Support to see if there are global issues with the application server hardware.

**Parent Topic:**[Resolving platform performance issues](resolving-plat-performance-issues.md)

