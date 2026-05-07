---
title: Creating custom events
description: Instrument trackable click-action events of your choice directly in the UI with no coding necessary. Tag DOM elements in Service Portal, Next Experience, CoreUI applications. Or derive new custom events from existing active events.
locale: en-US
release: australia
product: Usage Insights
classification: usage-insights
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Usage Insights, Usage Insights, Platform Analytics]
---

# Creating custom events

Instrument trackable click-action events of your choice directly in the UI with no coding necessary. Tag DOM elements in Service Portal, Next Experience, CoreUI applications. Or derive new custom events from existing active events.

## Before you begin

Role required: analytics\_admin, analytics\_viewer, or analytics\_instrumenter

## About this task

The visual tagging framework is a no-code, UI-based solution. It enables you to see how users interact with your features. Track how users engage with each feature and which buttons they select by cataloging each possible event with just a few simple selections in the UI. 

## Procedure

1.  Navigate to the page in which you would like to track your click action.

2.  In the Usage Insights page overlay panel, select **Instrumentation tab**&gt;**Start instrumentation**.![select instrumentation tab](../image/usage-insights-event-tagging-instrumentation-tab.png)

    If your page overlay tab isn't already open, you can find it in the main toolbar.![Page overlay tab](../image/usage-insights-event-tagging-page-overlay.png)

    The page shifts to instrumentation mode and you can select the UI element that you want to tag, for example, buttons, links, tabs, or icons. Selecting each one shows you the name of the element and asks if you want to create an event for it or dismiss it. You can also see whether this element is already being tracked or not \(excluding cataloged events\).

3.  If you want to create an event for an element you selected, select **Add instrumentation**.![Tag an event](../image/usage-insights-event-tagging-element-unique.png)

    The Instrumentation tab then enables you to define the event name and description and displays the element’s properties \(ID, text, aria-label, DOM path\). You can add or edit event details and event properties to capture additional context. For example, element type, location in the DOM, and custom attributes. The instrumentation tab also displays a window telling you whether your event exists and isn’t unique. If you see this window, it's best not to create a duplicate, identical event.

4.  Input the specifications you want and select **Save**.![Save and create an event](../image/usage-insights-event-tagging-event-creation.png)

    Now, the event is visually tagged and immediately available for tracking in Usage Insights. The overlay panel shows all currently tagged events on the page, including their status and occurrence counts. After approval, the tagged event becomes part of the official cataloged event set. The event is available for tracking in customer instances, promoting consistent adoption metrics and analytics coverage.

5.  Review and validate each event.

    Use the Instrumentation tab to view the list of active tagged events. Select your newly created event to review its properties and historical trend data \(if available\). Validate that the event is firing as expected by interacting with the tagged element and checking for event data in Usage Insights.

6.  Apply advanced practices.

    Avoid duplicating events: Check if your event exists before you create it. Review the [existing list](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2775777) of Usage Insights events before creating a custom event. Use meaningful, unique event names and descriptions for clarity.


## What to do next

[See the event inventory](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2775777)- a catalog of all existing custom events.

**Note:** If you want to capture a user action not related to a click on your page \(for example, a Page View\), you can use the [SNAnalytics API](https://developer.servicenow.com/dev.do#!/reference/api/zurich/client/SNAnalyticsClientAPI).

**Parent Topic:**[Using Usage Insights](../content-framework/concept/using-uxa.md)

**Related topics**  


[Viewing events analytics](view-events.md#)

