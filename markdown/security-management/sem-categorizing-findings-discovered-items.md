---
title: Categorizing findings and discovered items using classification rules
description: Classification groups automate the classification of entities or records based on the classification rules defined in the group. The condition for each rule is evaluated in order, and the first matching rule is used.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Automating prioritization and triaging, Security Exposure Management workflow, Explore, Unified Security Exposure Management, Security Operations]
---

# Categorizing findings and discovered items using classification rules

Classification groups automate the classification of entities or records based on the classification rules defined in the group. The condition for each rule is evaluated in order, and the first matching rule is used.

The Unified Security Exposure Management base system includes the following two classification groups, which classify discovered items and vulnerabilities respectively:

-   Technologies Classification
-   Discovered Containers Classification
-   Configuration Tests Classification
-   CWEs Classification
-   Test Groups Classification
-   Discovered Applications Classification
-   Discovered Items Classification
-   Vulnerability Entries Classification

Whenever findings and discovered items are imported, the vulnerability classification rules in the respective groups are executed. Based on the conditions set in the rule, the records are classified into the relevant classification group. You can create, edit, delete, or reapply these rules to an existing vulnerability.

**Note:**

-   For a selected table, there can only be one active classification group.
-   Once you create a group, you can’t delete it.

**Parent Topic:**[Automating prioritization and triaging](sem-automating-prioritization-triaging.md)

**Related topics**  


[Configuring classification rules](sem-configure-classification-rules.md#)

