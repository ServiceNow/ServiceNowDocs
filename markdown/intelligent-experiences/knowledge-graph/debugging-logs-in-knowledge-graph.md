---
title: Analyze Knowledge Graph logs for debugging
description: Review Knowledge Graph logs and history to analyze performance and diagnose issues.
locale: en-US
release: australia
product: Knowledge Graph
classification: knowledge-graph
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [generative AI, Now Assist]
breadcrumb: [Test a Knowledge Graph schema, Using Knowledge Graph Designer, Knowledge Graph, Enable AI experiences]
---

# Analyze Knowledge Graph logs for debugging

Review Knowledge Graph logs and history to analyze performance and diagnose issues.

## Before you begin

Ensure that you do not make any changes to the production instance.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **sys\_properties.list** &gt; **sn\_kg.log.level** or **All** &gt; **System Properties** &gt; **All Properties** &gt; **sn\_kg.log.level**.

2.  Open **sn\_kg.log.level** and in the value field add `debug`.

    The default value is **Err** but you can use any of the following values:

    -   emerg
    -   alert
    -   crit
    -   err
    -   warning
    -   notice
    -   info
    -   debug
3.  Select **Update**.

    The logs will now be added to **syslog**.


