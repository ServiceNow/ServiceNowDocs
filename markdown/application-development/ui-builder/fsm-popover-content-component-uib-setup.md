---
title: Field service popover component setup
description: Field service popover component displays additional content for an object in a popover in the field service pages.Define the headings, field data objects, and the header actions objects of your Field service popover component with these properties.Select event handlers to configure the actions \(events\) provided with the Field service popover component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/fsm-popover-content-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Field service popover component setup

Field service popover component displays additional content for an object in a popover in the field service pages.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Field service popover that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md). For instructions on using the content tree, see [UI Builder tutorial](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-tutorial.md).

    \[Omitted image "fsm-popover-content-content-tree.png"\] Alt text: Image showing FSM Popover Content content tree

2.  Select the Field service popover component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Field service popover label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Field service popover component properties

Define the headings, field data objects, and the header actions objects of your Field service popover component with these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

|Field|Property|Description|
|-----|--------|-----------|
|Heading|heading|Title of the card or the popover|
|Subheading|subheading|Subtitle of the card or the popover|
|Field data object|popoverFieldData|List of field values that are displayed on the card or the popover|
|Header actions object|headerActions|Card or popover actions and overflow actions displayed in the card or popover header|
|Context data object|contextData|Optional contextual data used in action payloads|
|Width|width|Width of the label value pair table in popover|

## Field service popover component events

Select event handlers to configure the actions \(events\) provided with the Field service popover component.

The Events tab shows the events used by the Field service popover component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Field service popover actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

|Event|Description|
|-----|-----------|
|SN\_FSM\_POPOVER\#ACTION\_CLICKED|Action dispatched when the card is clicked|
|SN\_FSM\_POPOVER\#OVERFLOW\_ACTION\_CLICKED|Action dispatched when the overflow action is clicked|
|DECLARATIVE\_ACTION|Action dispatched when the declarative action is clicked|

