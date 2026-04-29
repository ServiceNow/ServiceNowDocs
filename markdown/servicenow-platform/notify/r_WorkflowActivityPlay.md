---
title: Play workflow activity
description: The Play activity plays a sound file on a Notify call.
locale: en-US
release: australia
product: Notify
classification: notify
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Notify workflow activities, Notify reference, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Play workflow activity

The **Play** activity plays a sound file on a Notify call.

## Input Variables

Input variables determine the initial behavior of the activity.

|Variable|Description|
|--------|-----------|
|URL|Enter the URL of a sound file to play. If the URL is inaccessible, or if the audio file mime type is not supported by the telephony provider, the **play** activity is skipped.|
|Loop|Enter the number of times the sound file should play.|

## Conditions

The conditions determine which transition comes after this activity. The **play** activity does not specify any conditions by default.

You can create an error condition to handle errors with the sound file. The activity transitions through the error condition if the specified sound file is not available, or has an unsupported mime type. Supported mime types are listed on the Notify Audio MIME Types \[notify\_mime\_type\] table.

**Parent Topic:**[Notify workflow activities](../concept/c_NotifyActivities.md)

