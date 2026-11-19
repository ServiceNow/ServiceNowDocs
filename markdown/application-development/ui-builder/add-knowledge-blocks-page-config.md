---
title: Add Knowledge Blocks page template configuration
description: The Add Knowledge Blocks component enables you to search for, create, and view knowledge blocks in an article. Add Knowledge Blocks is used in the contextual sidebar for a Knowledge form.Configure related properties for the Add Knowledge Blocks component.Select event handlers to configure the actions \(events\) provided with the Add Knowledge Blocks component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/add-knowledge-blocks-page-config.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Add Knowledge Blocks page template configuration

The Add Knowledge Blocks component enables you to search for, create, and view knowledge blocks in an article. Add Knowledge Blocks is used in the contextual sidebar for a Knowledge form.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Add Knowledge Blocks component that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Work with pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "knowledge-blocks-connected-content-tree.png"\] Alt text: Add Knowledge Blocks connected content tree.

2.  Select the Add Knowledge Blocks component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Add Knowledge Blocks label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Add Knowledge Blocks page template properties

Configure related properties for the Add Knowledge Blocks component.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

|Field|Property|Description|
|-----|--------|-----------|
|Table|table|The parent table.|
|Sys ID|sysId|The sys ID of the article to add the knowledge block to.|
|Fields|fields|The field names and values fetched from the parent record.|

## Add Knowledge Blocks page template events

Select event handlers to configure the actions \(events\) provided with the Add Knowledge Blocks component.

The Events tab shows the events used by the Add Knowledge Blocks component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Add Knowledge Blocks actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

|Event|Description|
|-----|-----------|
|Open record|Open a record in a workspace sub tab.|

