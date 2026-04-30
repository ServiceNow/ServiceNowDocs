---
title: Instance cache effects on performance
description: Minimize actions that purge and rebuild the instance cache during core business hours to avoid performance degradation during peak hours.
locale: en-US
release: zurich
product: Platform Performance
classification: platform-performance
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Resolve issues, Platform performance, Maintain and monitor, Administer]
---

# Instance cache effects on performance

Minimize actions that purge and rebuild the instance cache during core business hours to avoid performance degradation during peak hours.

Performance degrades whenever you purge and rebuild the instance cache. During core business hours, avoid or minimize any of the following actions that purge and rebuild the instance cache.

-   Adding or updating system properties
-   Adding or updating dictionary entries
-   Committing update sets
-   Adding or updating translations

**Parent Topic:**[Resolving platform performance issues](resolving-plat-performance-issues.md)

