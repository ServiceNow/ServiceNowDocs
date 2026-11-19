---
title: Text link component setup
description: The Text link component provides a text label that opens relevant linked content when selected.Configure the source and appearance of the Text link component.Select event handlers to configure the actions \(events\) provided with the Text link component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/text-link-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Text link component setup

The Text link component provides a text label that opens relevant linked content when selected.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Text link that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).\[Omitted image "text-link-content-tree.png"\] Alt text: Shows the text link component in the content tree

2.  Select the Text link component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Text link label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Text link component properties

Configure the source and appearance of the Text link component.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

|Field|Property|Description|
|-----|--------|-----------|
|Label|label|The text that is displayed as a link. The default label is "Link" if no label is provided.|
|Variant|variant|Link style, including color and interaction behavior.|
|Link|href|The URL that opens when the user selects the text link.|
|Underlined|underlined|Option to underline the link at all times.|
|Open new window|opensWindow|Option to open the link in a new window or tab \(if the user's browser configuration permits\). "Link opens in new window" is announced to assistive technology users.|
|Filename override|download|Option to instruct the browser to download a file instead of opening a URL. Provide the value as a string to pre-populate the filename of the downloaded file.|
|ARIA properties|configAria|An object whose keys reference a specific HTML element within the component. The value of each key is an object that contains ARIA properties and corresponding values.|

## Text link component events

Select event handlers to configure the actions \(events\) provided with the Text link component.

The Events tab shows the events used by the Text link component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Text link actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

|Event|Description|
|-----|-----------|
|Text link clicked|Dispatched when the link is clicked.|

