---
title: Deleting stale findings automatically using auto-delete rules
description: Auto-delete rules automatically remove findings from the system based on predefined criteria. These rules help manage the life-cycle of vulnerabilities by ensuring that resolved or outdated findings are removed, reducing clutter and maintaining a clean, up-to-date database. This automation streamlines the vulnerability management process and ensures that teams focus on current and relevant issues.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Automating prioritization and triaging, Security Exposure Management workflow, Explore, Unified Security Exposure Management, Security Operations]
---

# Deleting stale findings automatically using auto-delete rules

Auto-delete rules automatically remove findings from the system based on predefined criteria. These rules help manage the life-cycle of vulnerabilities by ensuring that resolved or outdated findings are removed, reducing clutter and maintaining a clean, up-to-date database. This automation streamlines the vulnerability management process and ensures that teams focus on current and relevant issues.

Over time, a significant number of closed records can accumulate in the Findings tables in your ServiceNow instance. Many of these records may have been closed for more than 365 days but haven’t been removed. Using auto-delete rules can help you remove these older, closed records. Running these rules not only significantly reduces the number of records in the Findings tables but also helps maintain high performance.

By default, auto-delete rules target records that have been closed for 365 days. However, the first run might attempt to purge too many records in a single transaction, which can be problematic in larger environments. To avoid this issue, you may stagger the deletion process. For example, you could start by deleting records that are older than 450 days. Once that run is complete, you can gradually work your way down in smaller increments. For example, delete records older than 425, 400, 375 days until you have reduced the number of records older than 365 days.

**Parent Topic:**[Automating prioritization and triaging](sem-automating-prioritization-triaging.md)

**Related topics**  


[Configuring auto-delete rules](sem-configure-auto-delete-rules.md#)

