---
title: Event payloads in UI Builder
description: Use event payloads to link additional data to an action.
locale: en-US
release: xanadu
product: UI Builder
classification: ui-builder
topic_type: concept
last_updated: "2024-10-28"
reading_time_minutes: 1
breadcrumb: [Manage actions in UI Builder pages, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Event payloads in UI Builder

Use event payloads to link additional data to an action.

Event payloads are pieces of data sent by a component when a selected event is triggered. The data sent by an event can include the type of event, timestamps, user actions, or resource data such as a SysID.

You can use this payload data when configuring an event handler so that the resulting interaction can be linked to the emitted data. For example, a SysID can be passed to other components on a page to display information related to a specified record.

![Red box containing the available event payloads for the selected component.](../image/event-payloads-avaliable.png)

Each component and event has a unique set of payload options. Event payloads may not be properly defined for each component. If that is the case, define a client script so that the console logs payloads such as `console.log(event.payload)`.

**Parent Topic:**[Manage actions in UI Builder pages](work-events.md)

