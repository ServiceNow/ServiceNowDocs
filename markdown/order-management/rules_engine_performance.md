---
title: Optimizing rules engine performance
description: You can help make your pages responsive by following a few guidelines.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Optimizing rules engine performance

You can help make your pages responsive by following a few guidelines.

![Optimizing rules engine performance writeup](../images/cpq-rule-engine-performance.png)

In any online shopping or configuration experience, end-user engagement requires a responsive web page. CPQ achieves excellent performance as a result of its proprietary rules engine. CPQ also provides the following benefits:

-   The end user receives instantaneous feedback after every input change.
-   End users do not need to click an Update button for the configurator to evaluate their input. Administrators do not need to distinguish fields that automatically run from fields that must be updated through user interaction.
-   Because the rules engine evaluates the optimal rule order, rules do not have to manually ordered by the admin.

Although the CPQ rules engine is engineered to process rules quickly, not all rules perform the same. Therefore, the administrator plays an essential role in optimizing the performance of the CPQ UI. Use the following rules of thumb when you build rules:

-   Simple rules are best. The CPQ rules engine can quickly run tens of thousands of rules whose conditions have defined logical expressions and whose actions are defined without scripting.

    Reliance on unscripted rules allows the rules engine to determine the subset of rules that must be run in specific scenarios. Simple rules allow the rules engine to predictively optimize.

-   Avoid scripting, which degrades end-user performance.

    Configuration maintenance and extension engage numerous stakeholders, many of whom prioritize task completion over end-user performance. Experience with thousands of CPQ implementations shows that administrators often don't script with performance in mind. Even implementers who script optimally cannot prevent poor decisions by future administrators.

-   Table lookups adversely impact end-user performance.
    -   Table lookups feature inherent costs of query, matching against unbounded volumes of tabular data, and scripted post-processing of the retrieved data.
    -   In contrast, some CPQ vendors simplify administration by leveraging tabular data and scripts that query and process the tables, CPQ converts these tables to many simple rules. This conversion short-cuts the queries and post-processing, eliminates inefficient coding practices, and allows the rules engine to intelligently determine when a rule should run, and the specific tasks it must accomplish.

