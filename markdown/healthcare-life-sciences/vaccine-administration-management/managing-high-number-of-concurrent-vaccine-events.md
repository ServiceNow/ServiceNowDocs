---
title: Manage processing for a high number of concurrent vaccine events
description: Manage multiple parallel queues to help process vaccine events run in a parallel mode. You can distribute the vaccine queue events process to different nodes rather than keeping the load on a single node.
locale: en-US
release: australia
product: Vaccine Administration Management
classification: vaccine-administration-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Vaccine Administration Management, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Manage processing for a high number of concurrent vaccine events

Manage multiple parallel queues to help process vaccine events run in a parallel mode. You can distribute the vaccine queue events process to different nodes rather than keeping the load on a single node.

## Before you begin

Role required: sn\_vaccine\_sm.admin

## About this task

You can implement the vaccine queue events process flow in a parallel mode. With parallel processing, the job creates separate events for each vaccine queue. This processing helps distribute the events to all active nodes instead of being processed in a single node.

## Procedure

1.  In the navigation filter, enter `sys_trigger.list`.

2.  In the **Search** field, enter `*vaccine queue events process`.

3.  Select the vaccine queue events process record.

4.  Set the **System ID** field to **Active Nodes**.

5.  Click **Update**.

    This configuration creates multiple sys\_trigger records for each node.


**Parent Topic:**[Configuring Vaccine Administration Management](vaccine-mgmt-config.md)

