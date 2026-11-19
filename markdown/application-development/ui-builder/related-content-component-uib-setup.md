---
title: Related Content component setup
description: This component displays content in a simple list so that users can navigate to other content that might be helpful. The Related Content can be a list of items, snippets, and secondary information.Configure the items that appear in the related Related Content component.Select event handlers to configure the actions \(events\) provided with the Related Content component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/related-content-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Related Content component setup

This component displays content in a simple list so that users can navigate to other content that might be helpful. The Related Content can be a list of items, snippets, and secondary information.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Related Content that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md). For instructions on using the content tree, see [UI Builder tutorial](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-tutorial.md).

    \[Omitted image "related-content-content-tree.png"\] Alt text: Related Content component in content tree.

2.  Select the Related Content component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Related Content label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Related Content component properties

Configure the items that appear in the related Related Content component.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

|Field|Property|Description|
|-----|--------|-----------|
|Heading|heading|Text to describe the related content. For example, if you're using the component to display relevant help articles, you may enter `Related Articles`.|
|Items|items|List of related items that are displayed. The related items are organized as an array of objects.|
|Maximum number of items|maxItems|Maximum number of items to display in the component. If this field is set to zero, then all items are shown. This field is automatically set to 5.|
|Fields delimiter|fieldDelimiter|Delimiter that is used to visually separate the field information that is displayed for every related item. For example, assume that every related item has information about who wrote the item, how often it was viewed, and so on. If the delimiter is a dash -, then this information would be displayed as `Asked by Beth Anglin - 90 views - 0 Votes - 1 Answer`. This field is automatically set to the bullet • character.|
|No content message|noContentMessage|Message that appears when there is no content to display in the component. This field is automatically set to **No content to display**.|
|Hide if empty|hideIfEmpty|Option to hide the component if there is no content to display in the component. If you select this option, the `No content message` message does not appear.|

## Related Content component events

Select event handlers to configure the actions \(events\) provided with the Related Content component.

The Events tab shows the events used by the Related Content component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Related Content actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

|Event|Description|
|-----|-----------|
|Related content link clicked|User clicks a link. The payload contains the configuration of the content that you set in the component properties.|

