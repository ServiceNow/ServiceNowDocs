---
title: Record Tabs component setup
description: The Record Tabs component groups information into contextual tabs for organized viewing of records.Configure the route and tab properties with these properties.Select event handlers to configure the actions \(events\) provided with the Record Tabs component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/record-tabs-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Record Tabs component setup

The Record Tabs component groups information into contextual tabs for organized viewing of records.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Configure routes in the classic environment.

    Routes are the tabs configured to that appear in the Record Tabs set.

2.  Define a label for your Record Tabs that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "record-tabs-content-tree.png"\] Alt text: Record Tabs content tree.

3.  Select the Record Tabs component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Record Tabs label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Record Tabs component setup

Configure the route and tab properties with these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

|Field|Property|Description|
|-----|--------|-----------|
|Routes| |Record from the UX App Routes table that defines the component or screen and associated data to render on each tab.|
|Properties for detail tab| |Properties that define the fields and values to display on the Details section of the form.|
|Selected Tab|selectedTabIndex|Tab that opens when specified.|
|Related Lists Refresh Requests| |Request that refreshes Related Lists.|

## Record Tabs component events

Select event handlers to configure the actions \(events\) provided with the Record Tabs component.

The Events tab shows the events used by the Record Tabs component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Record Tabs actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

|Event|Description|
|-----|-----------|
|Add Notification|Action dispatched once the field declarative action execution has completed, notifying the user about its success or failure.|
|Remove notifications|Array of notification objects.|
|Clear notifications|Action to clear all notifications.|
|Preview Record|Primary navigation action that opens some content.|
|Item Selected|Primary navigation action that opens some content.|
|Screen Status Changed|Action dispatched to indicate that the form is dirty.|
|Execute UI Action|Action dispatched to execute the specified UI Action.|
|Refresh Requested|Action dispatched on successful field declarative action execution for server script action. This action is only dispatched when the record contains fields with field decorators.|
|List Query|Query for the list.|
|List Page Updated|List paged updated.|
|List Limit Updated|Number of items in the list per page.|
|List Data Fetch Succeeded|Action dispatched once the form finished fetching data.|

