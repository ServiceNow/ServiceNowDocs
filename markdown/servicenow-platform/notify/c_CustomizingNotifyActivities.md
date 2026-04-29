---
title: Notify activity event handlers
description: Notify workflow activities provide JavaScript functions that are invoked automatically when your telephony provider broadcasts certain events.
locale: en-US
release: australia
product: Notify
classification: notify
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Notify workflow activities, Notify reference, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Notify activity event handlers

Notify workflow activities provide JavaScript functions that are invoked automatically when your telephony provider broadcasts certain events.

When the telephony provider broadcasts an event related to a Notify call, such as the caller hanging up, the event is processed by the workflow associated with that Notify call. All currently-executing Notify activities in that workflow invoke a JavaScript function associated with that event.

Not all activities that support an event provide a default event handler implementation. You can provide an implementation for those event handlers when creating custom Notify activities.

**Parent Topic:**[Notify workflow activities](../../../administer/workflow-activities/concept/c_NotifyActivities.md)

**Related topics**  


[Creating Notify activities](c_CreatingNotifyActivities.md)

[Available Notify activity event handlers](../reference/r_NotifyEventHandlerMatrix.md)

