---
title: Unlock workflow activity
description: The Unlock activity releases a lock that was previously placed by the Lock activity.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
---

# Unlock workflow activity

The **Unlock** activity releases a lock that was previously placed by the **Lock** activity.

To release a lock, specify the same lock key that was specified in the **Lock** activity. If the **Lock** activity had a **Duration** specified, and that duration has already passed, the lock will already be released.

## Input variables

Input variables determine the initial behavior of the activity.

|Field|Description|
|-----|-----------|
|Lock key|The Mutex key that releases the lock. This key must match the key specified by a **Lock** activity. For more information, see [Lock activity]().|

## States

The activity state tells the workflow engine what to do with the activity.

|State|Description|
|-----|-----------|
|Finished|The activity successfully released the lock.|

