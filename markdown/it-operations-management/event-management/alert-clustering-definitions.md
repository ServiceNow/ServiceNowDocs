---
title: Create an alert clustering definition
description: An alert clustering definition determines the conditions that must be met for invoking one or more alert clustering tags. Alert clustering tags enable you to create an alert group from fewer alerts.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Tag cluster alert grouping, Alert grouping types, Alert grouping, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Create an alert clustering definition

An alert clustering definition determines the conditions that must be met for invoking one or more alert clustering tags. Alert clustering tags enable you to create an alert group from fewer alerts.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

Determine the alerts to be compared with existing alerts by creating a filter for the alerts to match. Filtered alerts matching alerts that exist in the system based on the definition's alert clustering tags are gathered into an alert group.

-   A definition must have alert clustering tags associated with it.
-   When modifying or deleting an alert clustering tag, all definitions with the specified tag are updated accordingly.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Tag Based Alert Clustering Engine** &gt; **Alert Clustering Definitions**.

2.  Select **New**.

3.  Configure the fields on the [Event Management tag based alert clustering definition form](../reference/tag-based-alert-clustering-definition-form.md).

4.  Select **Save**.


## Result

The definition appears on the Tag Based Alert Clustering Definitions table. Alert groups that are created by this definition are created as Tag Cluster groups.

