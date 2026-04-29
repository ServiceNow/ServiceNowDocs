---
title: Disable network traffic-based alert grouping
description: Disable network traffic-based alert grouping to prevent alerts from being grouped solely by network activity, reducing noise during traffic spikes and ensuring critical issues stand out for quicker resolution.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Network traffic based alert grouping, Alert grouping types and creation methods, Alert grouping, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Disable network traffic-based alert grouping

Disable network traffic-based alert grouping to prevent alerts from being grouped solely by network activity, reducing noise during traffic spikes and ensuring critical issues stand out for quicker resolution.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Administration** &gt; **Alert Correlation Properties**.

2.  Clear that check box for the property Enable Network Traffic correlation \(**sa\_analytics.agg.query\_network\_traffic\_correlation\_enabled**\).

3.  Set the property **sa\_analytics.enable\_process\_mapping\_calculation** to false.


