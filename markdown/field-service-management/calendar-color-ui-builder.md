---
title: Customizing the calendar grid in Dispatcher Workspace with UI Builder
description: Change or add colors to the calendar grid to update your Dispatcher Workspace display so dispatchers can easily see when agents are available.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Customize Dispatcher Workspace, Dispatcher Workspace, CSM/FSM Configurable Workspace, Configure, Field Service Management]
---

# Customizing the calendar grid in Dispatcher Workspace with UI Builder

Change or add colors to the calendar grid to update your Dispatcher Workspace display so dispatchers can easily see when agents are available.

In Dispatcher Workspace, the default colors for the calendar grid are white to show that agents are available and gray that the agent is unavailable. You can customize these colors.

The calendar grid in Dispatcher Workspace is made using a property called markspans. Change the color of mark spans to change the color of the calendar grid. For more information, see [Calendar UIB Setup](https://developer.servicenow.com/dev.do#!/reference/next-experience/zurich/now-components/now-calendar/uib-setup), and scroll to the markspans property.

**Important:** Mark spans are the only property on the Calendar UIB Setup page that is supported in Dispatcher Workspace.

The following image shows an example of markspans in UI Builder that are used to define the color of the calendar grid in Dispatcher Workspace.

![UI Builder displaying the color markspans](../image/calendar-mark-span.png "Markspans in UI Builder")

