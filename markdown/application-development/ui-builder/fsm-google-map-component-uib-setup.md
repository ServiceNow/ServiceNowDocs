---
title: Field service Google Map component setup
description: The Field service Google Map component display a Google map with markers to help to visually identify locations of people, tasks, and objects.Define the map settings, google key to access maps and APIs, and map markers of the Field service Google Map component with these properties.Select event handlers to configure the actions \(events\) provided with the Field service Google Map component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/fsm-google-map-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Field service Google Map component setup

The Field service Google Map component display a Google map with markers to help to visually identify locations of people, tasks, and objects.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Field service Google Map that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "fsm-google-map-content-tree.png"\] Alt text: Image showing fsm google map content tree

2.  Select the Field service Google Map component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Field service Google Map label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Field service Google Map component properties

Define the map settings, google key to access maps and APIs, and map markers of the Field service Google Map component with these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

|Field|Property|Description|
|-----|--------|-----------|
|Map settings|mapSettings|Settings used to generate the Google map|
|Google key|googleKey|Key used too access google map and APIs|
|Selected record ID|selectedRecordId|Record ID of marker to highlight and center on in the map|
|Map markers|mapMarkers|List of objects that need to be displayed on the map|

## Field service Google Map component events

Select event handlers to configure the actions \(events\) provided with the Field service Google Map component.

The Events tab shows the events used by the Field service Google Map component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Field service Google Map actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

|Event|Description|
|-----|-----------|
|FSM\_GMAP\#MARKER\_ITEM\_CLICK|Action dispatched when a marked item is clicked|

