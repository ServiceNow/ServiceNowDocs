---
title: Create an alert clustering definition
description: Define alert clustering conditions to trigger one or more alert clustering tags, which help create alert groups from fewer alerts. Creating alert groups from fewer alerts reduces noise, making it easier to identify critical incidents, prioritize responses, and manage issues effectively.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Tag cluster alert grouping, Mixed alert grouping, Alert grouping types and creation methods, Alert grouping, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Create an alert clustering definition

Define alert clustering conditions to trigger one or more alert clustering tags, which help create alert groups from fewer alerts. Creating alert groups from fewer alerts reduces noise, making it easier to identify critical incidents, prioritize responses, and manage issues effectively.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

To create a tag def users need to use filter to define on which alerts the definition will apply and define a grouping criteria by specifying which field values should be compared to create a group.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Tag Based Alert Clustering Engine** &gt; **Alert Clustering Definitions**.

2.  Select **New**.

3.  Configure the fields on the [Event Management tag based alert grouping definition form](../reference/tag-based-alert-clustering-definition-form.md).

4.  Select **Save**.


## Result

The definition appears in the Tag Based Alert Clustering Definitions table and Service Operations Workspace \(ITOM\) &gt; Grouping automation. Alert groups created by this definition are categorized as Tag Cluster groups.

