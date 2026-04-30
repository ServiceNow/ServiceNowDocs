---
title: Record workflow activity
description: The Record workflow activity records audio from a user on a Notify call.
locale: en-US
release: zurich
product: Notify
classification: notify
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Notify workflow activities, Reference, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Record workflow activity

The **Record** workflow activity records audio from a user on a Notify call.

**Note:** The Record workflow activity records Notify call but not the Notify conference call. To record the Notify conference call, you can set the **Record** activity variable on the [Join Conference Call](r_WflowActivJoinConfCall.md) workflow activity.

## Input Variables

Input variables determine the initial behavior of the activity.

|Variable|Description|
|--------|-----------|
|Max duration \(in seconds\)|Enter the maximum duration, in seconds, allowed for a recording.|
|Timeout \(in seconds\)|Enter the amount of time to wait before ending a recording automatically when the caller is silent.|
|Finish Key|Specify the key a caller can press on their phone to end the recording.|

## Scratchpad Entries

The activity uses the workflow scratchpad to store persistent values.

The **record** activity adds the **recording** variable to the workflow scratchpad. This variable stores metadata about the recording, such as URl, ID, and duration. You can access the following values from this variable.

|Value|Description|
|-----|-----------|
|recording.recordingDuration|The duration of the recording, in seconds.|
|recording.from\_number|The caller's phone number, including country code.|
|recording.notify\_number|The Notify phone number used to respond to the call, including country code.|
|recording.recordingID|The ID used by the telephony provider to identify the recording.|
|recording.recordingURL|The URL from the telephony provider to access the recording.|

**Parent Topic:**[Notify workflow activities](../concept/c_NotifyActivities.md)

