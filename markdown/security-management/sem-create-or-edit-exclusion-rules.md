---
title: Create or edit exclusion rules
description: Create a rule to filter or exclude detections from getting converted into vulnerable items \(VITs\) during ingestion.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-11-18"
reading_time_minutes: 1
breadcrumb: [Configuring exclusion rules, Configure rules to manage findings, Implement, Unified Security Exposure Management, Security Operations]
---

# Create or edit exclusion rules

Create a rule to filter or exclude detections from getting converted into vulnerable items \(VITs\) during ingestion.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace**.

2.  Select **Administration** in the navigation pane.

3.  Select **Review** on the **Exclusion rules** tile.

4.  On the Rules page, select **Exclusion** in the navigation pane.

5.  Select **New** and fill in the fields on the form:

    |Field|Description|
    |-----|-----------|
    |Details|
    |Name|Name of the exclusion rule.|
    |Active|Option to activate the exclusion rule.|
    |Execution order|Unique order for each exclusion rule.|
    |Description|Description of the exclusion rule.|
    |If this condition is met|
    |Condition|Filter conditions for the detections that can be defined while processing them.|

6.  Select **Save**.

    Once an exclusion rule is created, it takes effect on detections starting from the subsequent ingestion.

7.  To edit, select the rule name and update the required fields and select **Update**.


