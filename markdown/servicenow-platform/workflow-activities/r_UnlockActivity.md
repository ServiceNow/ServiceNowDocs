---
title: Unlock workflow activity
description: The Unlock activity releases a lock that was previously placed by the Lock activity.
locale: en-US
release: australia
product: Workflow Activities
classification: workflow-activities
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Utility workflow activities, Workflow activities reference, Workflow activities, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Unlock workflow activity

The **Unlock** activity releases a lock that was previously placed by the **Lock** activity.

To release a lock, specify the same lock key that was specified in the **Lock** activity. If the **Lock** activity had a **Duration** specified, and that duration has already passed, the lock will already be released.

## Input variables

Input variables determine the initial behavior of the activity.

|Field|Description|
|-----|-----------|
|Lock key|The Mutex key that releases the lock. This key must match the key specified by a **Lock** activity. For more information, see [Lock activity](r_LockActivity-1.md).|

## States

The activity state tells the workflow engine what to do with the activity.

|State|Description|
|-----|-----------|
|Finished|The activity successfully released the lock.|

