---
title: Available Notify activity event handlers
description: When creating Notify workflow activities, you can use event-handler functions to respond to events from a telephony provider.
locale: en-US
release: xanadu
product: Notify
classification: notify
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Notify workflow activities, Reference, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Available Notify activity event handlers

When creating Notify workflow activities, you can use event-handler functions to respond to events from a telephony provider.

Not all activities or telephony providers support all events. For example, the **Reject** activity ends the call before the caller connects so the onNoAnswer function is never invoked from this activity.

**Note:** When configuring an activity to respond to an event, ensure that your telephony provider supports that event.

The following table describes available event handlers and lists the Notify workflow activities that can invoke each handler.

|Handler|Description|Activities|
|-------|-----------|----------|
|onExecute|Runs when the activity first runs.|All call-related activities|
|onUpdate|Runs when the call record associated with the workflow is updated.|All call-related activities|
|onCompleted|Runs when a call ends.|All call-related activities|
|onRinging|Runs when a call starts ringing.|Forward call, call, join conference call, forward to notify client|
|onInProgress|Runs when both parties are connected on a call.|Forward call, call, join conference call, forward to notify client|
|onNoAnswer|Runs when a call is not answered.|Forward call, call, join conference call, forward to notify client|
|onBusy|Runs when a called number is busy.|Forward call, call, join conference call, forward to notify client|
|onFailed|Runs when an error occurs.|All call-related activities|

**Parent Topic:**[Notify workflow activities](../../../administer/workflow-activities/concept/c_NotifyActivities.md)

