---
title: Record Header component setup
description: The Record Header displays record metadata that enables access to important fields from the record without having to search in the form.Configure the tables, values, and header images for your Record Header with these properties.Select event handlers to configure the actions \(events\) provided with the Record Header component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/record-header-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Record Header component setup

The Record Header displays record metadata that enables access to important fields from the record without having to search in the form.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Record Header that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "record-header-content-tree.png"\] Alt text: Record Header content tree.

2.  Select the Record Header component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Record Header label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Record Header component setup

Configure the tables, values, and header images for your Record Header with these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

|Field|Property|Description|
|-----|--------|-----------|
|Table|table|Table name for the record header.|
|Sys ID|sysId|Sys ID for the record header.|
|Primary value|primaryValue|Title that displays on the first row.|
|Subheading|subHeadingValue|Value shown as subheading under header.|
|Secondary values|secondaryItems|Array of key and value pairs for subtitles.|
|Header image|headerImageItem|Header item that describes image details.|
|Hide Tags|hideTagsValue|Option to disable the tags icon.|

## Record Header component events

Select event handlers to configure the actions \(events\) provided with the Record Header component.

The Events tab shows the events used by the Record Header component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Record Header actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

|Event|Description|
|-----|-----------|
|Preview Record|Action dispatched to preview a record.|

