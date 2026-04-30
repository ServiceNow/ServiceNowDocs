---
title: Unlock workflow activity
description: The Unlock activity releases a lock that was previously placed by the Lock activity.
locale: en-US
release: zurich
product: Workflow Activities
classification: workflow-activities
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Utility workflow activities, Workflow activities reference, Workflow activities, Classic Workflow, Build workflows]
---

# Unlock workflow activity

The **Unlock** activity releases a lock that was previously placed by the **Lock** activity.

To release a lock, specify the same lock key that was specified in the **Lock** activity. If the **Lock** activity had a **Duration** specified, and that duration has already passed, the lock will already be released.

## Input variables

Input variables determine the initial behavior of the activity.

|Field|Description|
|-----|-----------|
|Lock key|The Mutex key that releases the lock. This key must match the key specified by a **Lock** activity. For more information, see [Lock activity](https://www.servicenow.com/docs/access?context=r_LockActivity&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).|

## States

The activity state tells the workflow engine what to do with the activity.

|State|Description|
|-----|-----------|
|Finished|The activity successfully released the lock.|

