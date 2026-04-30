---
title: Configuring exclusion rules
description: By configuring exclusion rules, you can filter or exclude detections from being converted into vulnerable items \(VITs\) during ingestion. This filtering helps streamline vulnerability management by reducing noise and prioritizing critical issues.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure rules to manage findings, Implement, Unified Security Exposure Management, Security Operations]
---

# Configuring exclusion rules

By configuring exclusion rules, you can filter or exclude detections from being converted into vulnerable items \(VITs\) during ingestion. This filtering helps streamline vulnerability management by reducing noise and prioritizing critical issues.

## Execution order behavior

The execution order defines the priority in which exclusion rules are processed. Rules with a lower execution order value are evaluated first.

1.  Default execution order for new rules

    When you create an exclusion rule, the system automatically assigns an execution order to maintain spacing and avoid conflicts.

    System behavior:

    -   The first rule created: Execution order = 1000
    -   Subsequent rules: Execution order = \(highest existing execution order\) + 1000
2.  Updating execution order via drag

    In the Security Exposure Management Workspace, you can reorder exclusion rules using drag in the list view. When rules are repositioned, execution order values are recalculated automatically based on their new position.

    System behavior:

    -   Between two rules: New execution order = \(Order of previous rule + Order of next rule\) ÷ 2
    -   Moved to the top of the list: New execution order = \(Execution order of current top rule\) ÷ 2
    -   Moved to the bottom of the list: New execution order = \(Execution order of current bottom rule + 1000\)

**Related topics**  


[Controlling the ingestion volume with automatic exclusion](sem-controlling-ingestion-volume-automatic-exclusion.md)

